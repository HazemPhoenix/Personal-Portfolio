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
            "https://dhozvkf4o988s.cloudfront.net/u611q7%2Fpreview%2F65865349%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632857&Signature=bxOC8sSfeS3lwutT0cPwhZx7EVqk4pxYVAYypM5N40J4mdSLBUToKkWTIfRYZQXKgct3J8GDwFkrLjSw8-j6h8EN4FkIbHv5GfckXVbVfImjVoQQz9Gt-uVy5PEaVq7YpiIm-UJvQ7NuKL8Z9tNo2kpsTdpqAQjO1JDlF5nLPqGuYoZg7FZRTd984uh36G2KSGsQjOSY2sMjTX8UCQ7OytN56ik11FG5xrxuNzMXu9iSHKI0jmyPTQS2Xo6i4g1yoM9FU7z6K4wkSPuADHEI4yuQlJp5dp9rSMXVR9bnBHhRWIO~mtlANveowKJdLtOMtXmX95qasNpBxbEWIPMO6A__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
            "https://deyk7xhr3o4wv.cloudfront.net/p731q7%2Fpreview%2F65865351%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632875&Signature=XslRdFDdeNs5lIdaDlEKygZxKcmjLXEH-9o0OqcPtD-Pk1Uh5dPFAEF~SFawICYB~O3iTHSmXXL2~8C8CnQ7HgM7AV~fuMQ23ifeAzTZo5y0lwv5It7s1m8BC--jKuyP9cf~h-Qt8fFfhu1pIq6K4U9FoD8QJD2iJM0YeeyuwSDSLuSeon-~T3oEQjo7ITGsHtj56juDwYVEFZFC32RhDPmJJWfEljK7LpthcwCBfGhT-87ZJTojTi~DnrB0WVGGDDEoaAX4KLnVWefb1TOVKhcU~4Jh2nxnx6amOauvBCRMiLWWPxMBP3a2iPrwdzGQaL4sJj2RkHChKEOCqP5dVA__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
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
            "https://dhozvkf4o988s.cloudfront.net/u611q7%2Fpreview%2F65865349%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632857&Signature=bxOC8sSfeS3lwutT0cPwhZx7EVqk4pxYVAYypM5N40J4mdSLBUToKkWTIfRYZQXKgct3J8GDwFkrLjSw8-j6h8EN4FkIbHv5GfckXVbVfImjVoQQz9Gt-uVy5PEaVq7YpiIm-UJvQ7NuKL8Z9tNo2kpsTdpqAQjO1JDlF5nLPqGuYoZg7FZRTd984uh36G2KSGsQjOSY2sMjTX8UCQ7OytN56ik11FG5xrxuNzMXu9iSHKI0jmyPTQS2Xo6i4g1yoM9FU7z6K4wkSPuADHEI4yuQlJp5dp9rSMXVR9bnBHhRWIO~mtlANveowKJdLtOMtXmX95qasNpBxbEWIPMO6A__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
            "https://deyk7xhr3o4wv.cloudfront.net/p731q7%2Fpreview%2F65865351%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632875&Signature=XslRdFDdeNs5lIdaDlEKygZxKcmjLXEH-9o0OqcPtD-Pk1Uh5dPFAEF~SFawICYB~O3iTHSmXXL2~8C8CnQ7HgM7AV~fuMQ23ifeAzTZo5y0lwv5It7s1m8BC--jKuyP9cf~h-Qt8fFfhu1pIq6K4U9FoD8QJD2iJM0YeeyuwSDSLuSeon-~T3oEQjo7ITGsHtj56juDwYVEFZFC32RhDPmJJWfEljK7LpthcwCBfGhT-87ZJTojTi~DnrB0WVGGDDEoaAX4KLnVWefb1TOVKhcU~4Jh2nxnx6amOauvBCRMiLWWPxMBP3a2iPrwdzGQaL4sJj2RkHChKEOCqP5dVA__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
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
            "https://dhozvkf4o988s.cloudfront.net/u611q7%2Fpreview%2F65865349%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632857&Signature=bxOC8sSfeS3lwutT0cPwhZx7EVqk4pxYVAYypM5N40J4mdSLBUToKkWTIfRYZQXKgct3J8GDwFkrLjSw8-j6h8EN4FkIbHv5GfckXVbVfImjVoQQz9Gt-uVy5PEaVq7YpiIm-UJvQ7NuKL8Z9tNo2kpsTdpqAQjO1JDlF5nLPqGuYoZg7FZRTd984uh36G2KSGsQjOSY2sMjTX8UCQ7OytN56ik11FG5xrxuNzMXu9iSHKI0jmyPTQS2Xo6i4g1yoM9FU7z6K4wkSPuADHEI4yuQlJp5dp9rSMXVR9bnBHhRWIO~mtlANveowKJdLtOMtXmX95qasNpBxbEWIPMO6A__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
            "https://deyk7xhr3o4wv.cloudfront.net/p731q7%2Fpreview%2F65865351%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632875&Signature=XslRdFDdeNs5lIdaDlEKygZxKcmjLXEH-9o0OqcPtD-Pk1Uh5dPFAEF~SFawICYB~O3iTHSmXXL2~8C8CnQ7HgM7AV~fuMQ23ifeAzTZo5y0lwv5It7s1m8BC--jKuyP9cf~h-Qt8fFfhu1pIq6K4U9FoD8QJD2iJM0YeeyuwSDSLuSeon-~T3oEQjo7ITGsHtj56juDwYVEFZFC32RhDPmJJWfEljK7LpthcwCBfGhT-87ZJTojTi~DnrB0WVGGDDEoaAX4KLnVWefb1TOVKhcU~4Jh2nxnx6amOauvBCRMiLWWPxMBP3a2iPrwdzGQaL4sJj2RkHChKEOCqP5dVA__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
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
            "https://dhozvkf4o988s.cloudfront.net/u611q7%2Fpreview%2F65865349%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632857&Signature=bxOC8sSfeS3lwutT0cPwhZx7EVqk4pxYVAYypM5N40J4mdSLBUToKkWTIfRYZQXKgct3J8GDwFkrLjSw8-j6h8EN4FkIbHv5GfckXVbVfImjVoQQz9Gt-uVy5PEaVq7YpiIm-UJvQ7NuKL8Z9tNo2kpsTdpqAQjO1JDlF5nLPqGuYoZg7FZRTd984uh36G2KSGsQjOSY2sMjTX8UCQ7OytN56ik11FG5xrxuNzMXu9iSHKI0jmyPTQS2Xo6i4g1yoM9FU7z6K4wkSPuADHEI4yuQlJp5dp9rSMXVR9bnBHhRWIO~mtlANveowKJdLtOMtXmX95qasNpBxbEWIPMO6A__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
            "https://deyk7xhr3o4wv.cloudfront.net/p731q7%2Fpreview%2F65865351%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632875&Signature=XslRdFDdeNs5lIdaDlEKygZxKcmjLXEH-9o0OqcPtD-Pk1Uh5dPFAEF~SFawICYB~O3iTHSmXXL2~8C8CnQ7HgM7AV~fuMQ23ifeAzTZo5y0lwv5It7s1m8BC--jKuyP9cf~h-Qt8fFfhu1pIq6K4U9FoD8QJD2iJM0YeeyuwSDSLuSeon-~T3oEQjo7ITGsHtj56juDwYVEFZFC32RhDPmJJWfEljK7LpthcwCBfGhT-87ZJTojTi~DnrB0WVGGDDEoaAX4KLnVWefb1TOVKhcU~4Jh2nxnx6amOauvBCRMiLWWPxMBP3a2iPrwdzGQaL4sJj2RkHChKEOCqP5dVA__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
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
