---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279544"
---
# <span data-ttu-id="5983b-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="5983b-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="5983b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5983b-102">SYNOPSIS</span></span>
<span data-ttu-id="5983b-103">Blockzincirine üye oluşturma.</span><span class="sxs-lookup"><span data-stu-id="5983b-103">Create a blockchain member.</span></span>

## <span data-ttu-id="5983b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5983b-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5983b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5983b-105">DESCRIPTION</span></span>
<span data-ttu-id="5983b-106">Blockzincirine üye oluşturma.</span><span class="sxs-lookup"><span data-stu-id="5983b-106">Create a blockchain member.</span></span>

## <span data-ttu-id="5983b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5983b-107">EXAMPLES</span></span>

### <span data-ttu-id="5983b-108">Örnek 1: yeni blockzincirine üye oluşturma</span><span class="sxs-lookup"><span data-stu-id="5983b-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="5983b-109">Bu komut yeni bir blockzincirüyesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5983b-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="5983b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5983b-110">PARAMETERS</span></span>

### <span data-ttu-id="5983b-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="5983b-111">-AsJob</span></span>
<span data-ttu-id="5983b-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="5983b-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5983b-113">-Consortium</span><span class="sxs-lookup"><span data-stu-id="5983b-113">-Consortium</span></span>
<span data-ttu-id="5983b-114">Blockzincirine üye için konsorsiyum alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5983b-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="5983b-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="5983b-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="5983b-116">Managed Consortium yönetimi hesap parolasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5983b-116">Sets the managed consortium management account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5983b-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="5983b-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="5983b-118">Konsorsiyumun görünen adını alır.</span><span class="sxs-lookup"><span data-stu-id="5983b-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="5983b-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="5983b-119">-ConsortiumRole</span></span>
<span data-ttu-id="5983b-120">Konsorsiyumun üyesinin rolünü alır.</span><span class="sxs-lookup"><span data-stu-id="5983b-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="5983b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5983b-121">-DefaultProfile</span></span>
<span data-ttu-id="5983b-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5983b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5983b-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="5983b-123">-FirewallRule</span></span>
<span data-ttu-id="5983b-124">Yapılandırmak Için güvenlik duvarı kurallarını alır veya ayarlar, FIREWALLRULE özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5983b-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IFirewallRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5983b-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="5983b-125">-Location</span></span>
<span data-ttu-id="5983b-126">Blockzincir hizmetinin COĞRAFI konumu.</span><span class="sxs-lookup"><span data-stu-id="5983b-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="5983b-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="5983b-127">-Name</span></span>
<span data-ttu-id="5983b-128">Blockzincir üye adı.</span><span class="sxs-lookup"><span data-stu-id="5983b-128">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5983b-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5983b-129">-NoWait</span></span>
<span data-ttu-id="5983b-130">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="5983b-130">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5983b-131">-Parola</span><span class="sxs-lookup"><span data-stu-id="5983b-131">-Password</span></span>
<span data-ttu-id="5983b-132">Blockzincirine üyesinin temel auth parolasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5983b-132">Sets the basic auth password of the blockchain member.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5983b-133">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="5983b-133">-Protocol</span></span>
<span data-ttu-id="5983b-134">Blockzincirleri protokolünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5983b-134">Gets or sets the blockchain protocol.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Support.BlockchainProtocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5983b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5983b-135">-ResourceGroupName</span></span>
<span data-ttu-id="5983b-136">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5983b-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5983b-137">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5983b-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5983b-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="5983b-138">-Sku</span></span>
<span data-ttu-id="5983b-139">SKU adını alır veya ayarlar</span><span class="sxs-lookup"><span data-stu-id="5983b-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="5983b-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5983b-140">-SkuTier</span></span>
<span data-ttu-id="5983b-141">SKU katmanını alır veya ayarlar</span><span class="sxs-lookup"><span data-stu-id="5983b-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="5983b-142">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5983b-142">-SubscriptionId</span></span>
<span data-ttu-id="5983b-143">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="5983b-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5983b-144">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="5983b-144">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5983b-145">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5983b-145">-Tag</span></span>
<span data-ttu-id="5983b-146">Hizmetin, kaynağı tanımlayan anahtar değer çiftleri listesi olan etiketleri.</span><span class="sxs-lookup"><span data-stu-id="5983b-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5983b-147">-Validatornosuucapacity</span><span class="sxs-lookup"><span data-stu-id="5983b-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="5983b-148">Düğümlerin kapasitesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5983b-148">Gets or sets the nodes capacity.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5983b-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="5983b-149">-Confirm</span></span>
<span data-ttu-id="5983b-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5983b-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5983b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5983b-151">-WhatIf</span></span>
<span data-ttu-id="5983b-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5983b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5983b-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5983b-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5983b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5983b-154">CommonParameters</span></span>
<span data-ttu-id="5983b-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5983b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5983b-156">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5983b-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5983b-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5983b-157">INPUTS</span></span>

## <span data-ttu-id="5983b-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5983b-158">OUTPUTS</span></span>

### <span data-ttu-id="5983b-159">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. ıblockchainmember</span><span class="sxs-lookup"><span data-stu-id="5983b-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="5983b-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5983b-160">NOTES</span></span>

<span data-ttu-id="5983b-161">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="5983b-161">ALIASES</span></span>

<span data-ttu-id="5983b-162">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="5983b-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5983b-163">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5983b-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5983b-164">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5983b-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5983b-165">FIREWALLRULE <ıfirewallrule [] >: güvenlik duvarı kurallarını alır veya ayarlar</span><span class="sxs-lookup"><span data-stu-id="5983b-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="5983b-166">`[EndIPAddress <String>]`: Güvenlik duvarı kuralı aralığının bitiş IP adresini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5983b-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="5983b-167">`[RuleName <String>]`: Güvenlik Duvarı kurallarının adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5983b-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="5983b-168">`[StartIPAddress <String>]`: Güvenlik duvarı kuralı aralığının başlangıç IP adresini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5983b-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="5983b-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5983b-169">RELATED LINKS</span></span>

