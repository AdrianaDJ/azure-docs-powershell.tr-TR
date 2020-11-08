---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 42e5fb37cff49ab28f33cde4bf62b5c4b40c59a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279550"
---
# <span data-ttu-id="3b4c7-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="3b4c7-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="3b4c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b4c7-102">SYNOPSIS</span></span>
<span data-ttu-id="3b4c7-103">İşlem düğümünün ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="3b4c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b4c7-104">SYNTAX</span></span>

### <span data-ttu-id="3b4c7-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3b4c7-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3b4c7-106">Al</span><span class="sxs-lookup"><span data-stu-id="3b4c7-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3b4c7-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="3b4c7-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b4c7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b4c7-108">DESCRIPTION</span></span>
<span data-ttu-id="3b4c7-109">İşlem düğümünün ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="3b4c7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b4c7-110">EXAMPLES</span></span>

### <span data-ttu-id="3b4c7-111">Örnek 1: blockzincirine üyesi için liste işlem düğümleri</span><span class="sxs-lookup"><span data-stu-id="3b4c7-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="3b4c7-112">Bu komut, blockzincirine üyesi için işlem düğümlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="3b4c7-113">Örnek 2: işlem düğümü alma</span><span class="sxs-lookup"><span data-stu-id="3b4c7-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="3b4c7-114">Bu komut, işlem düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="3b4c7-115">Örnek 3: işlem düğümü alma</span><span class="sxs-lookup"><span data-stu-id="3b4c7-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="3b4c7-116">Bu komut, işlem düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="3b4c7-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b4c7-117">PARAMETERS</span></span>

### <span data-ttu-id="3b4c7-118">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="3b4c7-118">-BlockchainMemberName</span></span>
<span data-ttu-id="3b4c7-119">Blockzincir üye adı.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-119">Blockchain member name.</span></span>

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

### <span data-ttu-id="3b4c7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b4c7-120">-DefaultProfile</span></span>
<span data-ttu-id="3b4c7-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b4c7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b4c7-122">-InputObject</span></span>
<span data-ttu-id="3b4c7-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3b4c7-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="3b4c7-124">-Name</span></span>
<span data-ttu-id="3b4c7-125">İşlem düğümü adı.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4c7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b4c7-126">-ResourceGroupName</span></span>
<span data-ttu-id="3b4c7-127">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3b4c7-128">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3b4c7-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="3b4c7-129">-SubscriptionId</span></span>
<span data-ttu-id="3b4c7-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3b4c7-131">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-131">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4c7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b4c7-132">CommonParameters</span></span>
<span data-ttu-id="3b4c7-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b4c7-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b4c7-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b4c7-135">INPUTS</span></span>

### <span data-ttu-id="3b4c7-136">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. model. ıblockchainıdentity</span><span class="sxs-lookup"><span data-stu-id="3b4c7-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="3b4c7-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b4c7-137">OUTPUTS</span></span>

### <span data-ttu-id="3b4c7-138">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. ıctionnode</span><span class="sxs-lookup"><span data-stu-id="3b4c7-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="3b4c7-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b4c7-139">NOTES</span></span>

<span data-ttu-id="3b4c7-140">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="3b4c7-140">ALIASES</span></span>

<span data-ttu-id="3b4c7-141">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="3b4c7-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3b4c7-142">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3b4c7-143">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3b4c7-144">INPUTOBJECT <IBlockchainIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="3b4c7-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3b4c7-145">`[BlockchainMemberName <String>]`: Blockzincirine üye adı.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="3b4c7-146">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="3b4c7-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3b4c7-147">`[Location <String>]`: Konum adı.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="3b4c7-148">`[OperationId <String>]`: İşlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="3b4c7-149">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3b4c7-150">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3b4c7-151">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="3b4c7-152">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="3b4c7-153">`[TransactionNodeName <String>]`: İşlem düğümü adı.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="3b4c7-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b4c7-154">RELATED LINKS</span></span>

