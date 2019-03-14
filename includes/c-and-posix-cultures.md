---
ms.openlocfilehash: 92b3aa8ebf6a4c0d6968287fd09d84d4415d47f5
ms.sourcegitcommit: c58096d6814a25766abaf19020c7831e5c59ffc9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2019
ms.locfileid: "57665861"
---
> [!NOTE]
> <span data-ttu-id="adad6-101">**Выполнение .NET Core в только в системах Linux и macOS:** При использовании параметров сортировки для языков и региональных параметров C и Posix всегда учитывается регистр, так как в этом случае Юникод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="adad6-101">**.NET Core running on Linux and macOS systems only:** The collation behavior for the C and Posix cultures is always case-sensitive because these cultures do not use the expected Unicode collation order.</span></span> <span data-ttu-id="adad6-102">Мы не рекомендуем использовать язык и региональные параметры, выбранные для C или Posix, для выполнения операций сортировки с учетом языка и региональных параметров, но без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="adad6-102">We recommend that you use a culture other than C or Posix for performing culture-sensitive, case-insensitive sorting operations.</span></span>  
