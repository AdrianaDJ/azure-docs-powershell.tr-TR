---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277970"
---
# <span data-ttu-id="fd242-101">Az. destek modülü</span><span class="sxs-lookup"><span data-stu-id="fd242-101">Az.Support Module</span></span>
## <span data-ttu-id="fd242-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd242-102">Description</span></span>
<span data-ttu-id="fd242-103">Bu bölümdeki konular, Azure destek biletlerini Azure Resource Manager (ARM) çerçevesinde oluşturmak ve yönetmek için Azure PowerShell cmdlet 'lerini belgeleyin.</span><span class="sxs-lookup"><span data-stu-id="fd242-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="fd242-104">Microsoft. Azure. Commands. support ad alanında cmdlet 'ler var</span><span class="sxs-lookup"><span data-stu-id="fd242-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="fd242-105">Az. destek cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="fd242-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="fd242-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="fd242-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="fd242-107">Desteği sağlanan Azure hizmetlerinin geçerli listesini alır.</span><span class="sxs-lookup"><span data-stu-id="fd242-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="fd242-108">Her Azure hizmetinin, sorun sınıflandırması denen kendi kategorileri vardır.</span><span class="sxs-lookup"><span data-stu-id="fd242-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="fd242-109">Get-AzSupportProblemClassification kullanarak bir hizmetin geçerli sorun sınıflandırması listesini alın.</span><span class="sxs-lookup"><span data-stu-id="fd242-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="fd242-110">Yeni-AzSupportTicket kullanarak yeni bir destek bileti oluşturmak için hizmet ve sorun sınıflandırması GUID 'sini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fd242-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="fd242-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="fd242-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="fd242-112">Bir Azure hizmeti için geçerli sorun sınıflandırması listesini alır.</span><span class="sxs-lookup"><span data-stu-id="fd242-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="fd242-113">Yeni-AzSupportTicket kullanarak yeni bir destek bileti oluşturmak için hizmet ve sorun sınıflandırması GUID 'sini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fd242-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="fd242-114">Yeni-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="fd242-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="fd242-115">Destek kişi profili nesnesi oluşturmak için yardımcı cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd242-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="fd242-116">Bu nesneyi New-AzSupportTicket cmdlet için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fd242-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="fd242-117">Yeni-Azsupportbilet</span><span class="sxs-lookup"><span data-stu-id="fd242-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="fd242-118">Yeni bir Azure destek bileti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fd242-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="fd242-119">Bu işlem, Azure [Yeni destek isteği sayfasının](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)davranışındaki modellenir.</span><span class="sxs-lookup"><span data-stu-id="fd242-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="fd242-120">Get-Azsupportbilet</span><span class="sxs-lookup"><span data-stu-id="fd242-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="fd242-121">Destek biletleri listesini alır.</span><span class="sxs-lookup"><span data-stu-id="fd242-121">Gets the list of support tickets.</span></span> <span data-ttu-id="fd242-122">Bilet adına göre tam destek bileti alabilir veya destek biletlerini *duruma* veya *CreatedDate* 'e göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fd242-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="fd242-123">Update-Azsupportbilet</span><span class="sxs-lookup"><span data-stu-id="fd242-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="fd242-124">Destek biletinin önem derecesini, durumunu veya müşteri iletişim ayrıntılarını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="fd242-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="fd242-125">Get-Azsupportbilet Iletişimi</span><span class="sxs-lookup"><span data-stu-id="fd242-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="fd242-126">Destek bileti için iletişimleri alır.</span><span class="sxs-lookup"><span data-stu-id="fd242-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="fd242-127">*CreatedDate* veya *communicationtype* ile destek bileti iletişimini de filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fd242-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="fd242-128">Yeni-Azsupportbilet Iletişimi</span><span class="sxs-lookup"><span data-stu-id="fd242-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="fd242-129">Azure destek biletini yeni bir müşteri iletişimi ekler.</span><span class="sxs-lookup"><span data-stu-id="fd242-129">Adds a new customer communication to an Azure support ticket.</span></span> 



