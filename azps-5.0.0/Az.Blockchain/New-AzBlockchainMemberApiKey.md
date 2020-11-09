---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323413"
---
# <span data-ttu-id="86e79-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="86e79-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="86e79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86e79-102">SYNOPSIS</span></span>
<span data-ttu-id="86e79-103">Blockzincirine üye için API anahtarlarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="86e79-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="86e79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="86e79-104">SYNTAX</span></span>

### <span data-ttu-id="86e79-105">Regenerategenişletilen (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="86e79-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="86e79-106">Regenerateviaıdentitygenişletilen</span><span class="sxs-lookup"><span data-stu-id="86e79-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="86e79-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="86e79-107">DESCRIPTION</span></span>
<span data-ttu-id="86e79-108">Blockzincirine üye için API anahtarlarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="86e79-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="86e79-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="86e79-109">EXAMPLES</span></span>

### <span data-ttu-id="86e79-110">Örnek 1: ad kullanan blockzincirine üyesinin API anahtarlarını yeniden üret</span><span class="sxs-lookup"><span data-stu-id="86e79-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="86e79-111">Bu komut, ad, kaynak grubu kullanarak blockzincirine üye için API anahtarlarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="86e79-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="86e79-112">Örnek 2: tanımlayıcıların kullanıldığı blockzincirine üye için API anahtarlarını yeniden üret</span><span class="sxs-lookup"><span data-stu-id="86e79-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="86e79-113">Bu komut, kimlik kullanan blockzincirine üye için API anahtarlarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="86e79-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="86e79-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="86e79-114">PARAMETERS</span></span>

### <span data-ttu-id="86e79-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="86e79-115">-BlockchainMemberName</span></span>
<span data-ttu-id="86e79-116">Blockzincir üye adı.</span><span class="sxs-lookup"><span data-stu-id="86e79-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="86e79-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86e79-117">-DefaultProfile</span></span>
<span data-ttu-id="86e79-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="86e79-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86e79-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86e79-119">-InputObject</span></span>
<span data-ttu-id="86e79-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="86e79-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="86e79-121">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="86e79-121">-KeyName</span></span>
<span data-ttu-id="86e79-122">API anahtarı adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="86e79-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="86e79-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86e79-123">-ResourceGroupName</span></span>
<span data-ttu-id="86e79-124">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="86e79-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="86e79-125">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86e79-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="86e79-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="86e79-126">-SubscriptionId</span></span>
<span data-ttu-id="86e79-127">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="86e79-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="86e79-128">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="86e79-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="86e79-129">-Değer</span><span class="sxs-lookup"><span data-stu-id="86e79-129">-Value</span></span>
<span data-ttu-id="86e79-130">API anahtar değerini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="86e79-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="86e79-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="86e79-131">-Confirm</span></span>
<span data-ttu-id="86e79-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="86e79-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86e79-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86e79-133">-WhatIf</span></span>
<span data-ttu-id="86e79-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="86e79-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86e79-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="86e79-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86e79-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e79-136">CommonParameters</span></span>
<span data-ttu-id="86e79-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="86e79-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e79-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="86e79-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e79-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="86e79-139">INPUTS</span></span>

### <span data-ttu-id="86e79-140">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. model. ıblockchainıdentity</span><span class="sxs-lookup"><span data-stu-id="86e79-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="86e79-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="86e79-141">OUTPUTS</span></span>

### <span data-ttu-id="86e79-142">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. ıapıkey</span><span class="sxs-lookup"><span data-stu-id="86e79-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="86e79-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="86e79-143">NOTES</span></span>

<span data-ttu-id="86e79-144">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="86e79-144">ALIASES</span></span>

<span data-ttu-id="86e79-145">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="86e79-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="86e79-146">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="86e79-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="86e79-147">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="86e79-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="86e79-148">INPUTOBJECT <IBlockchainIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="86e79-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="86e79-149">`[BlockchainMemberName <String>]`: Blockzincirine üye adı.</span><span class="sxs-lookup"><span data-stu-id="86e79-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="86e79-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="86e79-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="86e79-151">`[Location <String>]`: Konum adı.</span><span class="sxs-lookup"><span data-stu-id="86e79-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="86e79-152">`[OperationId <String>]`: İşlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="86e79-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="86e79-153">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="86e79-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="86e79-154">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86e79-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="86e79-155">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="86e79-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="86e79-156">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="86e79-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="86e79-157">`[TransactionNodeName <String>]`: İşlem düğümü adı.</span><span class="sxs-lookup"><span data-stu-id="86e79-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="86e79-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="86e79-158">RELATED LINKS</span></span>

