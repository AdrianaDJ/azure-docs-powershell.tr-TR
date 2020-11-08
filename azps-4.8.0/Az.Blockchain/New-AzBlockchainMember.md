---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109161"
---
# <span data-ttu-id="fb600-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="fb600-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="fb600-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb600-102">SYNOPSIS</span></span>
<span data-ttu-id="fb600-103">Blockzincirine üye oluşturma.</span><span class="sxs-lookup"><span data-stu-id="fb600-103">Create a blockchain member.</span></span>

## <span data-ttu-id="fb600-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb600-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fb600-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb600-105">DESCRIPTION</span></span>
<span data-ttu-id="fb600-106">Blockzincirine üye oluşturma.</span><span class="sxs-lookup"><span data-stu-id="fb600-106">Create a blockchain member.</span></span>

## <span data-ttu-id="fb600-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb600-107">EXAMPLES</span></span>

### <span data-ttu-id="fb600-108">Örnek 1: yeni blockzincirine üye oluşturma</span><span class="sxs-lookup"><span data-stu-id="fb600-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="fb600-109">Bu komut yeni bir blockzincirüyesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb600-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="fb600-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb600-110">PARAMETERS</span></span>

### <span data-ttu-id="fb600-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="fb600-111">-AsJob</span></span>
<span data-ttu-id="fb600-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="fb600-112">Run the command as a job</span></span>

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

### <span data-ttu-id="fb600-113">-Consortium</span><span class="sxs-lookup"><span data-stu-id="fb600-113">-Consortium</span></span>
<span data-ttu-id="fb600-114">Blockzincirine üye için konsorsiyum alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fb600-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="fb600-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="fb600-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="fb600-116">Managed Consortium yönetimi hesap parolasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fb600-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="fb600-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="fb600-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="fb600-118">Konsorsiyumun görünen adını alır.</span><span class="sxs-lookup"><span data-stu-id="fb600-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="fb600-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="fb600-119">-ConsortiumRole</span></span>
<span data-ttu-id="fb600-120">Konsorsiyumun üyesinin rolünü alır.</span><span class="sxs-lookup"><span data-stu-id="fb600-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="fb600-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb600-121">-DefaultProfile</span></span>
<span data-ttu-id="fb600-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb600-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb600-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="fb600-123">-FirewallRule</span></span>
<span data-ttu-id="fb600-124">Yapılandırmak Için güvenlik duvarı kurallarını alır veya ayarlar, FIREWALLRULE özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fb600-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="fb600-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="fb600-125">-Location</span></span>
<span data-ttu-id="fb600-126">Blockzincir hizmetinin COĞRAFI konumu.</span><span class="sxs-lookup"><span data-stu-id="fb600-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="fb600-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb600-127">-Name</span></span>
<span data-ttu-id="fb600-128">Blockzincir üye adı.</span><span class="sxs-lookup"><span data-stu-id="fb600-128">Blockchain member name.</span></span>

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

### <span data-ttu-id="fb600-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fb600-129">-NoWait</span></span>
<span data-ttu-id="fb600-130">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="fb600-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fb600-131">-Parola</span><span class="sxs-lookup"><span data-stu-id="fb600-131">-Password</span></span>
<span data-ttu-id="fb600-132">Blockzincirine üyesinin temel auth parolasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fb600-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="fb600-133">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="fb600-133">-Protocol</span></span>
<span data-ttu-id="fb600-134">Blockzincirleri protokolünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fb600-134">Gets or sets the blockchain protocol.</span></span>

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

### <span data-ttu-id="fb600-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb600-135">-ResourceGroupName</span></span>
<span data-ttu-id="fb600-136">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fb600-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fb600-137">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb600-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="fb600-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="fb600-138">-Sku</span></span>
<span data-ttu-id="fb600-139">SKU adını alır veya ayarlar</span><span class="sxs-lookup"><span data-stu-id="fb600-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="fb600-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="fb600-140">-SkuTier</span></span>
<span data-ttu-id="fb600-141">SKU katmanını alır veya ayarlar</span><span class="sxs-lookup"><span data-stu-id="fb600-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="fb600-142">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="fb600-142">-SubscriptionId</span></span>
<span data-ttu-id="fb600-143">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="fb600-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fb600-144">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="fb600-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fb600-145">Etiketli</span><span class="sxs-lookup"><span data-stu-id="fb600-145">-Tag</span></span>
<span data-ttu-id="fb600-146">Hizmetin, kaynağı tanımlayan anahtar değer çiftleri listesi olan etiketleri.</span><span class="sxs-lookup"><span data-stu-id="fb600-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="fb600-147">-Validatornosuucapacity</span><span class="sxs-lookup"><span data-stu-id="fb600-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="fb600-148">Düğümlerin kapasitesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fb600-148">Gets or sets the nodes capacity.</span></span>

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

### <span data-ttu-id="fb600-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb600-149">-Confirm</span></span>
<span data-ttu-id="fb600-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb600-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb600-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb600-151">-WhatIf</span></span>
<span data-ttu-id="fb600-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb600-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb600-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb600-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb600-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb600-154">CommonParameters</span></span>
<span data-ttu-id="fb600-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb600-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb600-156">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fb600-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb600-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb600-157">INPUTS</span></span>

## <span data-ttu-id="fb600-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb600-158">OUTPUTS</span></span>

### <span data-ttu-id="fb600-159">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. ıblockchainmember</span><span class="sxs-lookup"><span data-stu-id="fb600-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="fb600-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb600-160">NOTES</span></span>

<span data-ttu-id="fb600-161">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="fb600-161">ALIASES</span></span>

<span data-ttu-id="fb600-162">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="fb600-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fb600-163">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fb600-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fb600-164">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fb600-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fb600-165">FIREWALLRULE <ıfirewallrule [] >: güvenlik duvarı kurallarını alır veya ayarlar</span><span class="sxs-lookup"><span data-stu-id="fb600-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="fb600-166">`[EndIPAddress <String>]`: Güvenlik duvarı kuralı aralığının bitiş IP adresini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fb600-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="fb600-167">`[RuleName <String>]`: Güvenlik Duvarı kurallarının adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fb600-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="fb600-168">`[StartIPAddress <String>]`: Güvenlik duvarı kuralı aralığının başlangıç IP adresini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fb600-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="fb600-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb600-169">RELATED LINKS</span></span>

