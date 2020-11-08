---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279558"
---
# <span data-ttu-id="f15a8-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="f15a8-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="f15a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f15a8-102">SYNOPSIS</span></span>
<span data-ttu-id="f15a8-103">Blockzincirine üye hakkında ayrıntılı bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="f15a8-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="f15a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f15a8-104">SYNTAX</span></span>

### <span data-ttu-id="f15a8-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f15a8-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f15a8-106">Al</span><span class="sxs-lookup"><span data-stu-id="f15a8-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f15a8-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="f15a8-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f15a8-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="f15a8-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f15a8-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="f15a8-109">DESCRIPTION</span></span>
<span data-ttu-id="f15a8-110">Blockzincirine üye hakkında ayrıntılı bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="f15a8-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="f15a8-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f15a8-111">EXAMPLES</span></span>

### <span data-ttu-id="f15a8-112">Örnek 1: liste blockzincirüyeleri</span><span class="sxs-lookup"><span data-stu-id="f15a8-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="f15a8-113">Bu komut, bir aboneliğin altındaki blockzincirine üye listeler.</span><span class="sxs-lookup"><span data-stu-id="f15a8-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="f15a8-114">Örnek 2: liste blockzincir üyeleri</span><span class="sxs-lookup"><span data-stu-id="f15a8-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="f15a8-115">Bu komut, kaynak grubu altındaki blockzincirine üye listeler.</span><span class="sxs-lookup"><span data-stu-id="f15a8-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="f15a8-116">Örnek 3: blockzincirine üye alma</span><span class="sxs-lookup"><span data-stu-id="f15a8-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="f15a8-117">Bu komut, kaynak grubu altında blockzincirine üye alır.</span><span class="sxs-lookup"><span data-stu-id="f15a8-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="f15a8-118">Örnek 4: blockzincirine üye alma</span><span class="sxs-lookup"><span data-stu-id="f15a8-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="f15a8-119">Bu komut, kaynak grubu altında blockzincirine üye alır.</span><span class="sxs-lookup"><span data-stu-id="f15a8-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="f15a8-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f15a8-120">PARAMETERS</span></span>

### <span data-ttu-id="f15a8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f15a8-121">-DefaultProfile</span></span>
<span data-ttu-id="f15a8-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f15a8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15a8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f15a8-123">-InputObject</span></span>
<span data-ttu-id="f15a8-124">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f15a8-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f15a8-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="f15a8-125">-Name</span></span>
<span data-ttu-id="f15a8-126">Blockzincir üye adı.</span><span class="sxs-lookup"><span data-stu-id="f15a8-126">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15a8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f15a8-127">-ResourceGroupName</span></span>
<span data-ttu-id="f15a8-128">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f15a8-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f15a8-129">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f15a8-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15a8-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f15a8-130">-SubscriptionId</span></span>
<span data-ttu-id="f15a8-131">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="f15a8-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f15a8-132">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="f15a8-132">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15a8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f15a8-133">CommonParameters</span></span>
<span data-ttu-id="f15a8-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f15a8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f15a8-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f15a8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f15a8-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f15a8-136">INPUTS</span></span>

### <span data-ttu-id="f15a8-137">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. model. ıblockchainıdentity</span><span class="sxs-lookup"><span data-stu-id="f15a8-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="f15a8-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f15a8-138">OUTPUTS</span></span>

### <span data-ttu-id="f15a8-139">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. ıblockchainmember</span><span class="sxs-lookup"><span data-stu-id="f15a8-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="f15a8-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f15a8-140">NOTES</span></span>

<span data-ttu-id="f15a8-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="f15a8-141">ALIASES</span></span>

<span data-ttu-id="f15a8-142">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="f15a8-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f15a8-143">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f15a8-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f15a8-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f15a8-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f15a8-145">INPUTOBJECT <IBlockchainIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="f15a8-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f15a8-146">`[BlockchainMemberName <String>]`: Blockzincirine üye adı.</span><span class="sxs-lookup"><span data-stu-id="f15a8-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="f15a8-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="f15a8-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f15a8-148">`[Location <String>]`: Konum adı.</span><span class="sxs-lookup"><span data-stu-id="f15a8-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="f15a8-149">`[OperationId <String>]`: İşlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="f15a8-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="f15a8-150">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f15a8-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f15a8-151">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f15a8-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f15a8-152">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="f15a8-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="f15a8-153">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="f15a8-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="f15a8-154">`[TransactionNodeName <String>]`: İşlem düğümü adı.</span><span class="sxs-lookup"><span data-stu-id="f15a8-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="f15a8-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f15a8-155">RELATED LINKS</span></span>

