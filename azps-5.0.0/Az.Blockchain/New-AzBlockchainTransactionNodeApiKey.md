---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 6f39e869137996a64c5fc440ee0c2c8bb559542b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277652"
---
# <span data-ttu-id="bf341-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="bf341-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="bf341-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf341-102">SYNOPSIS</span></span>
<span data-ttu-id="bf341-103">Blockzincirine üyesinin API anahtarlarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bf341-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="bf341-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf341-104">SYNTAX</span></span>

### <span data-ttu-id="bf341-105">Regenerategenişletilen (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf341-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bf341-106">Regenerateviaıdentitygenişletilen</span><span class="sxs-lookup"><span data-stu-id="bf341-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bf341-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf341-107">DESCRIPTION</span></span>
<span data-ttu-id="bf341-108">Blockzincirine üyesinin API anahtarlarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bf341-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="bf341-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf341-109">EXAMPLES</span></span>

### <span data-ttu-id="bf341-110">Örnek 1: ad kullanan bir işlem düğümü için API anahtarlarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bf341-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="bf341-111">Bu komut, ad, kaynak grubu kullanarak işlem düğümü için API anahtarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf341-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="bf341-112">Örnek 2: işlem düğümü için API anahtarlarını yeniden üret</span><span class="sxs-lookup"><span data-stu-id="bf341-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="bf341-113">Bu komut, bir işlem düğümü için, ıdenity kullanan API anahtarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf341-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="bf341-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf341-114">PARAMETERS</span></span>

### <span data-ttu-id="bf341-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="bf341-115">-BlockchainMemberName</span></span>
<span data-ttu-id="bf341-116">Blockzincir üye adı.</span><span class="sxs-lookup"><span data-stu-id="bf341-116">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf341-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf341-117">-DefaultProfile</span></span>
<span data-ttu-id="bf341-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf341-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf341-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf341-119">-InputObject</span></span>
<span data-ttu-id="bf341-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf341-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf341-121">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="bf341-121">-KeyName</span></span>
<span data-ttu-id="bf341-122">API anahtarı adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bf341-122">Gets or sets the API key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf341-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf341-123">-ResourceGroupName</span></span>
<span data-ttu-id="bf341-124">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bf341-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="bf341-125">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf341-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf341-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="bf341-126">-SubscriptionId</span></span>
<span data-ttu-id="bf341-127">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="bf341-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="bf341-128">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="bf341-128">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf341-129">-Transactiondüğüdynamicsnav:////runpage</span><span class="sxs-lookup"><span data-stu-id="bf341-129">-TransactionNodeName</span></span>
<span data-ttu-id="bf341-130">İşlem düğümü adı.</span><span class="sxs-lookup"><span data-stu-id="bf341-130">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf341-131">-Değer</span><span class="sxs-lookup"><span data-stu-id="bf341-131">-Value</span></span>
<span data-ttu-id="bf341-132">API anahtar değerini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bf341-132">Gets or sets the API key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf341-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="bf341-133">-Confirm</span></span>
<span data-ttu-id="bf341-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bf341-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf341-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf341-135">-WhatIf</span></span>
<span data-ttu-id="bf341-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf341-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf341-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bf341-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf341-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf341-138">CommonParameters</span></span>
<span data-ttu-id="bf341-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf341-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf341-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bf341-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf341-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf341-141">INPUTS</span></span>

### <span data-ttu-id="bf341-142">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. model. ıblockchainıdentity</span><span class="sxs-lookup"><span data-stu-id="bf341-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="bf341-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf341-143">OUTPUTS</span></span>

### <span data-ttu-id="bf341-144">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. ıapıkey</span><span class="sxs-lookup"><span data-stu-id="bf341-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="bf341-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf341-145">NOTES</span></span>

<span data-ttu-id="bf341-146">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="bf341-146">ALIASES</span></span>

<span data-ttu-id="bf341-147">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="bf341-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bf341-148">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bf341-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bf341-149">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bf341-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bf341-150">INPUTOBJECT <IBlockchainIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="bf341-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bf341-151">`[BlockchainMemberName <String>]`: Blockzincirine üye adı.</span><span class="sxs-lookup"><span data-stu-id="bf341-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="bf341-152">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="bf341-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bf341-153">`[Location <String>]`: Konum adı.</span><span class="sxs-lookup"><span data-stu-id="bf341-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="bf341-154">`[OperationId <String>]`: İşlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="bf341-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="bf341-155">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bf341-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="bf341-156">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf341-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="bf341-157">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="bf341-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="bf341-158">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="bf341-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="bf341-159">`[TransactionNodeName <String>]`: İşlem düğümü adı.</span><span class="sxs-lookup"><span data-stu-id="bf341-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="bf341-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf341-160">RELATED LINKS</span></span>

