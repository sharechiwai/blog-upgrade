---
title: Enable spell check on Chrome
date: 2022-01-29
summary: This post share how to enable spell checker on Chrome
---
## Spell Checker on Chrome
hope you find it useful

```js
for (let i = 0; i < contacts.length; i++) {
      const contact = contacts[i];
      await prisma.sleekflow_contact.upsert({
        where: {
          id: contact.id,
        },
        update: {
          firstname: contact.FirstName,
          lastname: contact.LastName,
          company_name: contact.CompanyName,
          email: contact.Email,
          tel: contact.PhoneNumber,
          room_no: contact.RoomNo,
          created_at: contact.CreatedAt,
          updated_at: lastUpdated,
        },
        create: {
          id: contact.id,
          firstname: contact.FirstName,
          lastname: contact.LastName,
          company_name: contact.CompanyName,
          email: contact.Email,
          tel: contact.PhoneNumber,
          room_no: contact.RoomNo,
          created_at: contact.CreatedAt,
          updated_at: lastUpdated,
        },
      });
    }
    console.log('completed');
    console.log(new Date());



    
    const collection = await prisma.$transaction(
      contacts.map((contact) =>
        prisma.sleekflow_contact.upsert({
          where: {
            id: contact.id,
          },
          update: {
            firstname: contact.FirstName,
            lastname: contact.LastName,
            company_name: contact.CompanyName,
            email: contact.Email,
            tel: contact.PhoneNumber,
            room_no: contact.RoomNo,
            created_at: contact.CreatedAt,
            updated_at: lastUpdated,
          },
          create: {
            id: contact.id,
            firstname: contact.FirstName,
            lastname: contact.LastName,
            company_name: contact.CompanyName,
            email: contact.Email,
            tel: contact.PhoneNumber,
            room_no: contact.RoomNo,
            created_at: contact.CreatedAt,
            updated_at: lastUpdated,
          },
        }),
      ),
    );

    return collection;
```