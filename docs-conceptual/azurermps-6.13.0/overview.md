---
title: Azure PowerShell’e Genel Bakış | Microsoft Docs
description: Yükleme ve yapılandırma bağlantılarıyla birlikte Azure PowerShell’e genel bakış.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/20/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 5b5d3a9ff1ebdd5b170d83510300b310e2061887
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89242231"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="ccbe9-103">Azure PowerShell’e Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="ccbe9-103">Overview of Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="ccbe9-104">Azure PowerShell, Azure kaynaklarınızı yönetmek için [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modelini kullanan bir dizi cmdlet sunar.</span><span class="sxs-lookup"><span data-stu-id="ccbe9-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="ccbe9-105">[Azure Cloud Shell](/azure/cloud-shell/overview) ile tarayıcınızda kullanabilir veya yerel makinenize yükleyip herhangi bir PowerShell oturumunda kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ccbe9-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="ccbe9-106">[Cloud Shell](/azure/cloud-shell/overview)’i kullanarak Azure PowerShell’i tarayıcınızda çalıştırın veya kendi bilgisayarınıza [yükleyin](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="ccbe9-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="ccbe9-107">Daha sonra, hizmeti kullanmaya başlamak için [Başlangıç](get-started-azureps.md) makalesini okuyun.</span><span class="sxs-lookup"><span data-stu-id="ccbe9-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="ccbe9-108">En son sürüm hakkında bilgi edinmek için [sürüm notlarına](release-notes-azureps.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="ccbe9-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="ccbe9-109">Aşağıdaki örnekler, yaygın senaryoları Azure PowerShell ile nasıl gerçekleştireceğinizi öğrenmenize yardımcı olabilir:</span><span class="sxs-lookup"><span data-stu-id="ccbe9-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

- [<span data-ttu-id="ccbe9-110">Linux Sanal Makineleri</span><span class="sxs-lookup"><span data-stu-id="ccbe9-110">Linux Virtual Machines</span></span>](https://docs.microsoft.com/azure/virtual-machines/linux/powershell-samples)
- [<span data-ttu-id="ccbe9-111">Windows Sanal Makineleri</span><span class="sxs-lookup"><span data-stu-id="ccbe9-111">Windows Virtual Machines</span></span>](https://docs.microsoft.com/azure/virtual-machines/windows/powershell-samples)
- [<span data-ttu-id="ccbe9-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="ccbe9-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
- [<span data-ttu-id="ccbe9-113">SQL Veritabanları</span><span class="sxs-lookup"><span data-stu-id="ccbe9-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="ccbe9-114">PowerShell temel bilgilerini öğrenme</span><span class="sxs-lookup"><span data-stu-id="ccbe9-114">Learn PowerShell basics</span></span>

<span data-ttu-id="ccbe9-115">PowerShell'i tanımıyorsanız, PowerShell'e giriş makalesi size yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="ccbe9-115">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

- [<span data-ttu-id="ccbe9-116">PowerShell’i yükleme</span><span class="sxs-lookup"><span data-stu-id="ccbe9-116">Installing PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
- [<span data-ttu-id="ccbe9-117">PowerShell öğrenme kaynakları</span><span class="sxs-lookup"><span data-stu-id="ccbe9-117">PowerShell learning resources</span></span>](/powershell/scripting/learn/more-powershell-learning)

<span data-ttu-id="ccbe9-118">Ayrıca şu videoyu izleyebilirsiniz: [PowerShell Temel Bilgileri: (Bölüm 1) PowerShell'i Kullanmaya Başlama](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="ccbe9-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="ccbe9-119">Microsoft Learn ile becerilerinizi geliştirin</span><span class="sxs-lookup"><span data-stu-id="ccbe9-119">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="ccbe9-120">PowerShell betiklerini kullanarak Azure görevlerini otomatikleştirme</span><span class="sxs-lookup"><span data-stu-id="ccbe9-120">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="ccbe9-121">Daha fazla etkileşimli öğrenme içeriği...</span><span class="sxs-lookup"><span data-stu-id="ccbe9-121">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="ccbe9-122">Diğer Azure PowerShell modülleri</span><span class="sxs-lookup"><span data-stu-id="ccbe9-122">Other Azure PowerShell modules</span></span>

- [<span data-ttu-id="ccbe9-123">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ccbe9-123">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
- [<span data-ttu-id="ccbe9-124">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="ccbe9-124">Azure Information Protection</span></span>](/powershell/azure/aip/)
- [<span data-ttu-id="ccbe9-125">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="ccbe9-125">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
- [<span data-ttu-id="ccbe9-126">Azure Elastik DB</span><span class="sxs-lookup"><span data-stu-id="ccbe9-126">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
