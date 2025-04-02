<template>
  <section class="mt-20 flex flex-col gap-5 md:gap-10" id="projects">
    <h2 class="text-center text-2xl md:text-5xl font-bold">
      A small selection of
      <span class="text-[#7519ff] dark:text-[#CBACF9]">recent projects</span>
    </h2>
    <div class="grid md:grid-cols-2 gap-5 md:w-11/12 md:mx-auto">
      <ProjectCard
        v-for="(project, index) in projects"
        :key="index"
        :src="project.imageUrl"
        :alt="project.title"
        :title="project.title"
        :description="project.description"
        :link="project.link"
        :technologies="project.technologies"
      />
    </div>
  </section>
</template>

<script>
import ProjectCard from "./RecentProjects/ProjectCard.vue";

export default {
  data() {
    return {
      projects: [
        {
          title: "Reservio",
          description:
            "Reservio is a web app that connects venue owners with customers seeking event spaces, enabling venue searches, availability checks, and online reservations.",
          imageUrl:
            "https://dz0i85a16ad4a.cloudfront.net/t8mmp7%2Fpreview%2F65864830%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632490&Signature=Rvo2KvYNKwqY0wU6z2MG8HL3WN~qozc7PqVVZ3L0X3S2paxJtrQumCZAS8efhl3pUlVv-7VN8lFz~YE9VK3bYxJEgFiFOZZ7ftsiPg57jmyF5hgFJQjBMdYnRGppO8hsriKvAiPh3gwS4htFoCrhT--mDVEM5rdRbPk-NfrImZLWQ6HGlvhmZNib4tH9ec~suT6mrQSJL7Uz13OBxhQ8bQ9cUFFhCRkdNOBIYKkpdFnF9Oy13iYPhw23uPdIrx~VBF7jDrLsP1aFgJq6LvCXpmcF62UjEphEMHtz2icZRJDMsE8rbciP1dLw73-TmQePMkWvzBPlaTClhwyHZPraFw__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
          link: "https://reservio-two.vercel.app/",
          technologies: [
            "https://dhozvkf4o988s.cloudfront.net/u611q7%2Fpreview%2F65865349%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743631997&Signature=b3Ft7TvSvmbUJiuKMreCFW4~1qCh8oBNMf6P1LDjH9AeL6xMw89GtIeF~ZXYVjAMf8UT3LAo7kQ~MsmRtTEpRtOtaIWUG3j1v2Dc-MTt7OY2OCIv7EHKXKPt8ypkBOzjRmd-Lacia0iNnOy5GxMatennSG1G6wIbcUvfRrVH-koxif906fz2MrJGDrOjemHL6VK6eC-6V-DJtk4UHOtO8V~Mo8-uHkQWmzSKM3xfdASdG8l21U6VTMAxFnGuuckzEfd8PTYqlY9RPY2-E6GMYLtWmTckCrCcq5AHzSKdc8wGcEuFOuuSBK-1tm9fcpMQj6Eq2PWL6qfGAazizSnf3g__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
            "https://deyk7xhr3o4wv.cloudfront.net/p731q7%2Fpreview%2F65865351%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632224&Signature=Js0I6zIwK429grAfNhVgfCPSnEvjI6MvBTgXlZe5osE3Vx8Wai3oA92i5VAL1ahkCBZcyEa38hkSzS8rROAStvdlInZdt0QSq1deUqC6HzMctGY0fwPBtLeShJHbuxuDbf18RguHJeUYHDqpgaXwOvzW7jCHahylNUbdjWNDyYKWys9ZbqDR4teYHmZh6855Rm2z~p3RtdDQMf4plMbSvjqc0PDiCyEGbDjTGjxl4WWRvaLaIQNw7i-WblQfdZ9b6F5OEmHVJXow1ryuTQMi-vL1MyFcq50dG-~Ca9jHFi1VxEonDrbhiQ-z9j5obNBRS8xojD39yMTLdzuuitn8Gg__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
            "https://d1ywz8thsltaos.cloudfront.net/p841q7%2Fpreview%2F65865352%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632296&Signature=Z5Vi84t23~NxW55BoTw-SQFEBA-WRLi5RJ2VFaCPOSb-4F36NekhtcfluRYwhuVVQDKfUr-FAfmZq9LjFbp5ETH10Yh4q4~xOv66EZeh~KbCBwQEKmQZxRtQ2GlcrsZ3WacOrvAsF7MP4liM-1hfUNLC09v-VlexW2P7ynzBcBYLg7mqYSZKM8cBjBbfTbVjahGCkaMa7hw-GkyIhnoVKicPJT3gq8wLp6jCGef-Xk9iUe3Xmw2h3NlZEHvHuIqpo7PlYDYWy9QANdyjsbrZJ4Kzu126NSoCXYB5Em9e~98qOp~qOV8R9Vp~bTROzxUocYGoSANHgly2~rL8WA6MNg__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
            "https://d243wifbt6aeh5.cloudfront.net/l861q7%2Fpreview%2F65865354%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632313&Signature=fkwWW9ZHWOWjrwTct9OJcdLMFyaN-u0raCgWNR10zv1A9KCWBr8Zc9Cosoj39WPM6IWKqISDDpErIjDHMPmeOiIJjLZW~j5U~HYcnpG8AT-LtK7HTBH0N7p0psemL1gSW6aLsWq4NfI3JS4~R25EwVnLD594tW7HP3KFqRap2wqa4KGZqpVBN~d-MO4RTeCitRn2oUpnUFgEUphaq5iJ5IF9m0~chlv-NEvQnG1fns3X4Fc4FgGKsEF~of5kk0y1AnBXPEqpqhCSacuHVBm8hpU8WNrI4x9sCPC9lqlTT9cXAFwWhcN39XMSjWHNtgpjvCvOhvEe3kxRCbJwzZlsqA__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
          ],
        },
        {
          title: "Reservio",
          description:
            "Reservio is a web app that connects venue owners with customers seeking event spaces, enabling venue searches, availability checks, and online reservations.",
          imageUrl:
            "https://dz0i85a16ad4a.cloudfront.net/t8mmp7%2Fpreview%2F65864830%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632490&Signature=Rvo2KvYNKwqY0wU6z2MG8HL3WN~qozc7PqVVZ3L0X3S2paxJtrQumCZAS8efhl3pUlVv-7VN8lFz~YE9VK3bYxJEgFiFOZZ7ftsiPg57jmyF5hgFJQjBMdYnRGppO8hsriKvAiPh3gwS4htFoCrhT--mDVEM5rdRbPk-NfrImZLWQ6HGlvhmZNib4tH9ec~suT6mrQSJL7Uz13OBxhQ8bQ9cUFFhCRkdNOBIYKkpdFnF9Oy13iYPhw23uPdIrx~VBF7jDrLsP1aFgJq6LvCXpmcF62UjEphEMHtz2icZRJDMsE8rbciP1dLw73-TmQePMkWvzBPlaTClhwyHZPraFw__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
          link: "https://reservio-two.vercel.app/",
          technologies: [
            "https://dhozvkf4o988s.cloudfront.net/u611q7%2Fpreview%2F65865349%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743631997&Signature=b3Ft7TvSvmbUJiuKMreCFW4~1qCh8oBNMf6P1LDjH9AeL6xMw89GtIeF~ZXYVjAMf8UT3LAo7kQ~MsmRtTEpRtOtaIWUG3j1v2Dc-MTt7OY2OCIv7EHKXKPt8ypkBOzjRmd-Lacia0iNnOy5GxMatennSG1G6wIbcUvfRrVH-koxif906fz2MrJGDrOjemHL6VK6eC-6V-DJtk4UHOtO8V~Mo8-uHkQWmzSKM3xfdASdG8l21U6VTMAxFnGuuckzEfd8PTYqlY9RPY2-E6GMYLtWmTckCrCcq5AHzSKdc8wGcEuFOuuSBK-1tm9fcpMQj6Eq2PWL6qfGAazizSnf3g__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
            "https://deyk7xhr3o4wv.cloudfront.net/p731q7%2Fpreview%2F65865351%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632224&Signature=Js0I6zIwK429grAfNhVgfCPSnEvjI6MvBTgXlZe5osE3Vx8Wai3oA92i5VAL1ahkCBZcyEa38hkSzS8rROAStvdlInZdt0QSq1deUqC6HzMctGY0fwPBtLeShJHbuxuDbf18RguHJeUYHDqpgaXwOvzW7jCHahylNUbdjWNDyYKWys9ZbqDR4teYHmZh6855Rm2z~p3RtdDQMf4plMbSvjqc0PDiCyEGbDjTGjxl4WWRvaLaIQNw7i-WblQfdZ9b6F5OEmHVJXow1ryuTQMi-vL1MyFcq50dG-~Ca9jHFi1VxEonDrbhiQ-z9j5obNBRS8xojD39yMTLdzuuitn8Gg__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
            "https://d1ywz8thsltaos.cloudfront.net/p841q7%2Fpreview%2F65865352%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632296&Signature=Z5Vi84t23~NxW55BoTw-SQFEBA-WRLi5RJ2VFaCPOSb-4F36NekhtcfluRYwhuVVQDKfUr-FAfmZq9LjFbp5ETH10Yh4q4~xOv66EZeh~KbCBwQEKmQZxRtQ2GlcrsZ3WacOrvAsF7MP4liM-1hfUNLC09v-VlexW2P7ynzBcBYLg7mqYSZKM8cBjBbfTbVjahGCkaMa7hw-GkyIhnoVKicPJT3gq8wLp6jCGef-Xk9iUe3Xmw2h3NlZEHvHuIqpo7PlYDYWy9QANdyjsbrZJ4Kzu126NSoCXYB5Em9e~98qOp~qOV8R9Vp~bTROzxUocYGoSANHgly2~rL8WA6MNg__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
            "https://d243wifbt6aeh5.cloudfront.net/l861q7%2Fpreview%2F65865354%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632313&Signature=fkwWW9ZHWOWjrwTct9OJcdLMFyaN-u0raCgWNR10zv1A9KCWBr8Zc9Cosoj39WPM6IWKqISDDpErIjDHMPmeOiIJjLZW~j5U~HYcnpG8AT-LtK7HTBH0N7p0psemL1gSW6aLsWq4NfI3JS4~R25EwVnLD594tW7HP3KFqRap2wqa4KGZqpVBN~d-MO4RTeCitRn2oUpnUFgEUphaq5iJ5IF9m0~chlv-NEvQnG1fns3X4Fc4FgGKsEF~of5kk0y1AnBXPEqpqhCSacuHVBm8hpU8WNrI4x9sCPC9lqlTT9cXAFwWhcN39XMSjWHNtgpjvCvOhvEe3kxRCbJwzZlsqA__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
          ],
        },
        {
          title: "Reservio",
          description:
            "Reservio is a web app that connects venue owners with customers seeking event spaces, enabling venue searches, availability checks, and online reservations.",
          imageUrl:
            "https://dz0i85a16ad4a.cloudfront.net/t8mmp7%2Fpreview%2F65864830%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632490&Signature=Rvo2KvYNKwqY0wU6z2MG8HL3WN~qozc7PqVVZ3L0X3S2paxJtrQumCZAS8efhl3pUlVv-7VN8lFz~YE9VK3bYxJEgFiFOZZ7ftsiPg57jmyF5hgFJQjBMdYnRGppO8hsriKvAiPh3gwS4htFoCrhT--mDVEM5rdRbPk-NfrImZLWQ6HGlvhmZNib4tH9ec~suT6mrQSJL7Uz13OBxhQ8bQ9cUFFhCRkdNOBIYKkpdFnF9Oy13iYPhw23uPdIrx~VBF7jDrLsP1aFgJq6LvCXpmcF62UjEphEMHtz2icZRJDMsE8rbciP1dLw73-TmQePMkWvzBPlaTClhwyHZPraFw__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
          link: "https://reservio-two.vercel.app/",
          technologies: [
            "https://dhozvkf4o988s.cloudfront.net/u611q7%2Fpreview%2F65865349%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743631997&Signature=b3Ft7TvSvmbUJiuKMreCFW4~1qCh8oBNMf6P1LDjH9AeL6xMw89GtIeF~ZXYVjAMf8UT3LAo7kQ~MsmRtTEpRtOtaIWUG3j1v2Dc-MTt7OY2OCIv7EHKXKPt8ypkBOzjRmd-Lacia0iNnOy5GxMatennSG1G6wIbcUvfRrVH-koxif906fz2MrJGDrOjemHL6VK6eC-6V-DJtk4UHOtO8V~Mo8-uHkQWmzSKM3xfdASdG8l21U6VTMAxFnGuuckzEfd8PTYqlY9RPY2-E6GMYLtWmTckCrCcq5AHzSKdc8wGcEuFOuuSBK-1tm9fcpMQj6Eq2PWL6qfGAazizSnf3g__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
            "https://deyk7xhr3o4wv.cloudfront.net/p731q7%2Fpreview%2F65865351%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632224&Signature=Js0I6zIwK429grAfNhVgfCPSnEvjI6MvBTgXlZe5osE3Vx8Wai3oA92i5VAL1ahkCBZcyEa38hkSzS8rROAStvdlInZdt0QSq1deUqC6HzMctGY0fwPBtLeShJHbuxuDbf18RguHJeUYHDqpgaXwOvzW7jCHahylNUbdjWNDyYKWys9ZbqDR4teYHmZh6855Rm2z~p3RtdDQMf4plMbSvjqc0PDiCyEGbDjTGjxl4WWRvaLaIQNw7i-WblQfdZ9b6F5OEmHVJXow1ryuTQMi-vL1MyFcq50dG-~Ca9jHFi1VxEonDrbhiQ-z9j5obNBRS8xojD39yMTLdzuuitn8Gg__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
            "https://d1ywz8thsltaos.cloudfront.net/p841q7%2Fpreview%2F65865352%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632296&Signature=Z5Vi84t23~NxW55BoTw-SQFEBA-WRLi5RJ2VFaCPOSb-4F36NekhtcfluRYwhuVVQDKfUr-FAfmZq9LjFbp5ETH10Yh4q4~xOv66EZeh~KbCBwQEKmQZxRtQ2GlcrsZ3WacOrvAsF7MP4liM-1hfUNLC09v-VlexW2P7ynzBcBYLg7mqYSZKM8cBjBbfTbVjahGCkaMa7hw-GkyIhnoVKicPJT3gq8wLp6jCGef-Xk9iUe3Xmw2h3NlZEHvHuIqpo7PlYDYWy9QANdyjsbrZJ4Kzu126NSoCXYB5Em9e~98qOp~qOV8R9Vp~bTROzxUocYGoSANHgly2~rL8WA6MNg__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
            "https://d243wifbt6aeh5.cloudfront.net/l861q7%2Fpreview%2F65865354%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632313&Signature=fkwWW9ZHWOWjrwTct9OJcdLMFyaN-u0raCgWNR10zv1A9KCWBr8Zc9Cosoj39WPM6IWKqISDDpErIjDHMPmeOiIJjLZW~j5U~HYcnpG8AT-LtK7HTBH0N7p0psemL1gSW6aLsWq4NfI3JS4~R25EwVnLD594tW7HP3KFqRap2wqa4KGZqpVBN~d-MO4RTeCitRn2oUpnUFgEUphaq5iJ5IF9m0~chlv-NEvQnG1fns3X4Fc4FgGKsEF~of5kk0y1AnBXPEqpqhCSacuHVBm8hpU8WNrI4x9sCPC9lqlTT9cXAFwWhcN39XMSjWHNtgpjvCvOhvEe3kxRCbJwzZlsqA__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
          ],
        },
        {
          title: "Reservio",
          description:
            "Reservio is a web app that connects venue owners with customers seeking event spaces, enabling venue searches, availability checks, and online reservations.",
          imageUrl:
            "https://dz0i85a16ad4a.cloudfront.net/t8mmp7%2Fpreview%2F65864830%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632490&Signature=Rvo2KvYNKwqY0wU6z2MG8HL3WN~qozc7PqVVZ3L0X3S2paxJtrQumCZAS8efhl3pUlVv-7VN8lFz~YE9VK3bYxJEgFiFOZZ7ftsiPg57jmyF5hgFJQjBMdYnRGppO8hsriKvAiPh3gwS4htFoCrhT--mDVEM5rdRbPk-NfrImZLWQ6HGlvhmZNib4tH9ec~suT6mrQSJL7Uz13OBxhQ8bQ9cUFFhCRkdNOBIYKkpdFnF9Oy13iYPhw23uPdIrx~VBF7jDrLsP1aFgJq6LvCXpmcF62UjEphEMHtz2icZRJDMsE8rbciP1dLw73-TmQePMkWvzBPlaTClhwyHZPraFw__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
          link: "https://reservio-two.vercel.app/",
          technologies: [
            "https://dhozvkf4o988s.cloudfront.net/u611q7%2Fpreview%2F65865349%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743631997&Signature=b3Ft7TvSvmbUJiuKMreCFW4~1qCh8oBNMf6P1LDjH9AeL6xMw89GtIeF~ZXYVjAMf8UT3LAo7kQ~MsmRtTEpRtOtaIWUG3j1v2Dc-MTt7OY2OCIv7EHKXKPt8ypkBOzjRmd-Lacia0iNnOy5GxMatennSG1G6wIbcUvfRrVH-koxif906fz2MrJGDrOjemHL6VK6eC-6V-DJtk4UHOtO8V~Mo8-uHkQWmzSKM3xfdASdG8l21U6VTMAxFnGuuckzEfd8PTYqlY9RPY2-E6GMYLtWmTckCrCcq5AHzSKdc8wGcEuFOuuSBK-1tm9fcpMQj6Eq2PWL6qfGAazizSnf3g__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
            "https://deyk7xhr3o4wv.cloudfront.net/p731q7%2Fpreview%2F65865351%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632224&Signature=Js0I6zIwK429grAfNhVgfCPSnEvjI6MvBTgXlZe5osE3Vx8Wai3oA92i5VAL1ahkCBZcyEa38hkSzS8rROAStvdlInZdt0QSq1deUqC6HzMctGY0fwPBtLeShJHbuxuDbf18RguHJeUYHDqpgaXwOvzW7jCHahylNUbdjWNDyYKWys9ZbqDR4teYHmZh6855Rm2z~p3RtdDQMf4plMbSvjqc0PDiCyEGbDjTGjxl4WWRvaLaIQNw7i-WblQfdZ9b6F5OEmHVJXow1ryuTQMi-vL1MyFcq50dG-~Ca9jHFi1VxEonDrbhiQ-z9j5obNBRS8xojD39yMTLdzuuitn8Gg__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
            "https://d1ywz8thsltaos.cloudfront.net/p841q7%2Fpreview%2F65865352%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632296&Signature=Z5Vi84t23~NxW55BoTw-SQFEBA-WRLi5RJ2VFaCPOSb-4F36NekhtcfluRYwhuVVQDKfUr-FAfmZq9LjFbp5ETH10Yh4q4~xOv66EZeh~KbCBwQEKmQZxRtQ2GlcrsZ3WacOrvAsF7MP4liM-1hfUNLC09v-VlexW2P7ynzBcBYLg7mqYSZKM8cBjBbfTbVjahGCkaMa7hw-GkyIhnoVKicPJT3gq8wLp6jCGef-Xk9iUe3Xmw2h3NlZEHvHuIqpo7PlYDYWy9QANdyjsbrZJ4Kzu126NSoCXYB5Em9e~98qOp~qOV8R9Vp~bTROzxUocYGoSANHgly2~rL8WA6MNg__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
            "https://d243wifbt6aeh5.cloudfront.net/l861q7%2Fpreview%2F65865354%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632313&Signature=fkwWW9ZHWOWjrwTct9OJcdLMFyaN-u0raCgWNR10zv1A9KCWBr8Zc9Cosoj39WPM6IWKqISDDpErIjDHMPmeOiIJjLZW~j5U~HYcnpG8AT-LtK7HTBH0N7p0psemL1gSW6aLsWq4NfI3JS4~R25EwVnLD594tW7HP3KFqRap2wqa4KGZqpVBN~d-MO4RTeCitRn2oUpnUFgEUphaq5iJ5IF9m0~chlv-NEvQnG1fns3X4Fc4FgGKsEF~of5kk0y1AnBXPEqpqhCSacuHVBm8hpU8WNrI4x9sCPC9lqlTT9cXAFwWhcN39XMSjWHNtgpjvCvOhvEe3kxRCbJwzZlsqA__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
          ],
        },
      ],
    };
  },
  components: {
    ProjectCard,
  },
};
</script>
