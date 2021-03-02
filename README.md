# Docker

docker คือ การจำลองสภาพเเวดล้อมของ Server ขึ้นมา เพื่อให้สามารถรัน Services ต่าง ๆ โดยจะคล้ายๆกับ Visual Machine เเต่สิ่งที่เเตกต่าง คือ จะใช้ทรัพยากรย์ของเครื่องที่น้อยกว่าเเละไม่ติดกับ Guest OS เเต่จะรันบน Docker Engine โดยจะจำลอง Container ขึ้นมา โดย Container เปรียบเหมือนกล่อง 1 กล่อง โดยกล่อง 1 กล่องนี้จะทำงานเป็น Server ให้บริการต่าง ๆ  
 ลักษณะของ Docker จะเเบ่ง Services ต่าง ๆ ออกเป็นกล่อง ๆ

## Docker Registry

คือ ที่เก็บของ Docker Images ที่คน Upload มาเก็บไว้เพื่อให้คนอื่นสามารถนำไปใช้งานต่อ

## Docker Images

เป็นเหมือนเเม่เเบบหรือพิมพ์เขียวให้กับ Container โดยใน Docker Images จะประกอบด้วย Container ต่าง ๆ ที่นิยามไว้ หรือ Container ต่าง ๆ ที่เราต้องการติดตั้งเพื่อให้บริการ โดยมีการตั้งค่า Container ต่าง ๆ ไว้เเล้ว เมื่อสร้าง Docker Images เสร็จเเล้วสามารถ Push หรือ Upload ไปเก็บบน Docker Registry ได้ด้วย เพื่อให้คนอื่นนำไปใช้งานต่อหรือ เราสามารถนำไปใช้งานในครั้งต่อไป

## Docker Container

ดังที่กล่าวมาข้างต้นว่า Container เปรียบเหมือนกล่อง 1 กล่อง ที่บรรจุ Service ต่าง ๆ คอยให้บริการกับผู้ใช้งาน อาจจะเป็น Application ที่นักพัฒนาจัดทำขึ้นมา หรือเป็น Server ที่ติดตั้งไว้ เพื่อให้บริการกับผู้ใช้งาน โดย Docker Container จะมีน้ำหนักเบากว่า Visual Machine มาก จำทำให้สามารถติดตั้งเเละ Start ขึ้นมาเพื่อใช้งานได้อย่างรวดเร็ว

## คำสั่งเบื้องต้น

```yml
docker images
```

ใช้ดู Images ที่มีในเครื่อง

```yml
docker pull <ชื่อ image ที่ต้องการ pull>
```

เป็นการดาวโหลด Image มาไว้ที่เครื่อง เพื่อใช้ในการติดตั้ง หรือ Run Image นั้น ๆ

```yml
docker container ls -a
```

ใช้ในการดู container ที่มีอยู่ในเครื่องของเรา

```yml
docker rmi <ชื่อของ image หรือ id ของ image>
```

ใช้ในการลบ image

```yaml
docker rm <ชื่อของ container>
```

ใช้ลบ container
