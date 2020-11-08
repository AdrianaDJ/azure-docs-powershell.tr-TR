---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277548"
---
# <span data-ttu-id="491c9-101">Az. ResourceMover modülü</span><span class="sxs-lookup"><span data-stu-id="491c9-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="491c9-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="491c9-102">Description</span></span>
<span data-ttu-id="491c9-103">Microsoft Azure PowerShell: ResourceMover cmdlet 'leri</span><span class="sxs-lookup"><span data-stu-id="491c9-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="491c9-104">Az. ResourceMover cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="491c9-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="491c9-105">Add-Azkaynakmovermoveresource</span><span class="sxs-lookup"><span data-stu-id="491c9-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="491c9-106">Taşıma koleksiyonundaki bir taşıma kaynağı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="491c9-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="491c9-107">Get-Azkaynakmovermovecollection</span><span class="sxs-lookup"><span data-stu-id="491c9-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="491c9-108">Taşıma koleksiyonunu alır.</span><span class="sxs-lookup"><span data-stu-id="491c9-108">Gets the move collection.</span></span>

### [<span data-ttu-id="491c9-109">Get-Azkaynakmovermoveresource</span><span class="sxs-lookup"><span data-stu-id="491c9-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="491c9-110">Kaynağı taşı.</span><span class="sxs-lookup"><span data-stu-id="491c9-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="491c9-111">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="491c9-111">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="491c9-112">Çözülmemiş bağımlılıkların listesini alır.</span><span class="sxs-lookup"><span data-stu-id="491c9-112">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="491c9-113">Invoke-Azkaynakmovercommit</span><span class="sxs-lookup"><span data-stu-id="491c9-113">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="491c9-114">İstek gövdesine dahil edilen kaynak kümesini kaydeder.</span><span class="sxs-lookup"><span data-stu-id="491c9-114">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="491c9-115">Kayıt işlemi, moveState 'in ' CommitPending ' veya ' CommitFailed ' 'taki moveResource 'ta tetiklenir, moveResource moveState 'in başarılı bir şekilde tamamlanması için geçiş yapma.</span><span class="sxs-lookup"><span data-stu-id="491c9-115">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="491c9-116">Kullanıcıya yardımcı olmak için, yalnızca validateOnly özelliği true olarak ayarlanmış olan işlem çağrı yapabilir.</span><span class="sxs-lookup"><span data-stu-id="491c9-116">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="491c9-117">Invoke-Azkaynakmoverdiscard</span><span class="sxs-lookup"><span data-stu-id="491c9-117">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="491c9-118">İstek gövdesine dahil edilen kaynak kümesini atar.</span><span class="sxs-lookup"><span data-stu-id="491c9-118">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="491c9-119">At işlemi, moveState ' CommitPending ' veya ' DiscardFailed ' içindeki moveResource 'da tetiklenir, moveResource moveState 'in başarılı bir şekilde tamamlanmasında MovePending 'a geçiş yapılır.</span><span class="sxs-lookup"><span data-stu-id="491c9-119">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="491c9-120">Kullanıcıya yardımcı olmak için, yalnızca validateOnly özelliği true olarak ayarlanmış olan işlem çağrı yapabilir.</span><span class="sxs-lookup"><span data-stu-id="491c9-120">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="491c9-121">Invoke-Azresourcesmoverınitiatetaþý</span><span class="sxs-lookup"><span data-stu-id="491c9-121">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="491c9-122">İstek gövdesine dahil edilen kaynak kümesini taşıma.</span><span class="sxs-lookup"><span data-stu-id="491c9-122">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="491c9-123">Taşıma işlemi, moveResource 'ın Slaytbekliyor ' veya ' MoveFailed 'tekilerilerilerilerilerileriyle tetiklenir, bu da moveResource.</span><span class="sxs-lookup"><span data-stu-id="491c9-123">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="491c9-124">Kullanıcıya yardımcı olmak için, yalnızca validateOnly özelliği true olarak ayarlanmış olan işlem çağrı yapabilir.</span><span class="sxs-lookup"><span data-stu-id="491c9-124">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="491c9-125">Invoke-Azkaynakmoverprepare</span><span class="sxs-lookup"><span data-stu-id="491c9-125">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="491c9-126">İstek gövdesine dahil edilen kaynak kümesine hazırlanmaya başlatır.</span><span class="sxs-lookup"><span data-stu-id="491c9-126">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="491c9-127">Prepare işlemi, moveState 'in ' PreparePending ' veya ' PrepareFailed ' işleminde bulunan moveResource 'dır, moveResource.</span><span class="sxs-lookup"><span data-stu-id="491c9-127">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="491c9-128">Kullanıcıya yardımcı olmak için, yalnızca validateOnly özelliği true olarak ayarlanmış olan işlem çağrı yapabilir.</span><span class="sxs-lookup"><span data-stu-id="491c9-128">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="491c9-129">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="491c9-129">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="491c9-130">Bir taşıma koleksiyonu oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="491c9-130">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="491c9-131">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="491c9-131">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="491c9-132">Taşıma koleksiyonunu siler.</span><span class="sxs-lookup"><span data-stu-id="491c9-132">Deletes a move collection.</span></span>

### [<span data-ttu-id="491c9-133">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="491c9-133">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="491c9-134">Taşıma koleksiyonundan taşıma kaynağı siler.</span><span class="sxs-lookup"><span data-stu-id="491c9-134">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="491c9-135">Resolve-Azkaynakmovermovecollectiondependency</span><span class="sxs-lookup"><span data-stu-id="491c9-135">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="491c9-136">Taşıma koleksiyonundaki Taşıveresoallerin bağımlılıklarını hesaplar, çözümler ve doğrular.</span><span class="sxs-lookup"><span data-stu-id="491c9-136">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

