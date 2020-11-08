---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 708ad613c2dbab7e7224dbd392809d9502c9b447
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109155"
---
# <span data-ttu-id="f1ab2-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="f1ab2-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="f1ab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="f1ab2-103">Blockzincirine üye güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-103">Update a blockchain member.</span></span>

## <span data-ttu-id="f1ab2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1ab2-104">SYNTAX</span></span>

### <span data-ttu-id="f1ab2-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f1ab2-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f1ab2-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="f1ab2-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f1ab2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1ab2-107">DESCRIPTION</span></span>
<span data-ttu-id="f1ab2-108">Blockzincirine üye güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-108">Update a blockchain member.</span></span>

## <span data-ttu-id="f1ab2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1ab2-109">EXAMPLES</span></span>

### <span data-ttu-id="f1ab2-110">Örnek 1: blockzincirine üye güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f1ab2-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="f1ab2-111">Bu komut blockzincirine üye güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="f1ab2-112">Örnek 2: blockzincir üyesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f1ab2-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="f1ab2-113">Bu komut blockzincirine üye güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="f1ab2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1ab2-114">PARAMETERS</span></span>

### <span data-ttu-id="f1ab2-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="f1ab2-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="f1ab2-116">Managed Consortium yönetimi hesap parolasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="f1ab2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1ab2-117">-DefaultProfile</span></span>
<span data-ttu-id="f1ab2-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1ab2-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="f1ab2-119">-FirewallRule</span></span>
<span data-ttu-id="f1ab2-120">Güvenlik duvarı kurallarını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="f1ab2-121">Oluşturmak için, FIREWALLRULE özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="f1ab2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1ab2-122">-InputObject</span></span>
<span data-ttu-id="f1ab2-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1ab2-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="f1ab2-124">-Name</span></span>
<span data-ttu-id="f1ab2-125">Blockzincir üye adı.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-125">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1ab2-126">-Parola</span><span class="sxs-lookup"><span data-stu-id="f1ab2-126">-Password</span></span>
<span data-ttu-id="f1ab2-127">İşlem düğümü DNS uç noktası temel kimlik doğrulama parolasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="f1ab2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1ab2-128">-ResourceGroupName</span></span>
<span data-ttu-id="f1ab2-129">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f1ab2-130">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1ab2-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f1ab2-131">-SubscriptionId</span></span>
<span data-ttu-id="f1ab2-132">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f1ab2-133">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-133">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1ab2-134">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f1ab2-134">-Tag</span></span>
<span data-ttu-id="f1ab2-135">Hizmetin, kaynağı tanımlayan anahtar değer çiftleri listesi olan etiketleri.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="f1ab2-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="f1ab2-136">-Confirm</span></span>
<span data-ttu-id="f1ab2-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1ab2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1ab2-138">-WhatIf</span></span>
<span data-ttu-id="f1ab2-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1ab2-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1ab2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1ab2-141">CommonParameters</span></span>
<span data-ttu-id="f1ab2-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1ab2-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1ab2-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1ab2-144">INPUTS</span></span>

### <span data-ttu-id="f1ab2-145">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. model. ıblockchainıdentity</span><span class="sxs-lookup"><span data-stu-id="f1ab2-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="f1ab2-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1ab2-146">OUTPUTS</span></span>

### <span data-ttu-id="f1ab2-147">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. ıblockchainmember</span><span class="sxs-lookup"><span data-stu-id="f1ab2-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="f1ab2-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1ab2-148">NOTES</span></span>

<span data-ttu-id="f1ab2-149">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="f1ab2-149">ALIASES</span></span>

<span data-ttu-id="f1ab2-150">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="f1ab2-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f1ab2-151">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f1ab2-152">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f1ab2-153">FIREWALLRULE <ıfirewallrule [] >: güvenlik duvarı kurallarını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="f1ab2-154">`[EndIPAddress <String>]`: Güvenlik duvarı kuralı aralığının bitiş IP adresini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="f1ab2-155">`[RuleName <String>]`: Güvenlik Duvarı kurallarının adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="f1ab2-156">`[StartIPAddress <String>]`: Güvenlik duvarı kuralı aralığının başlangıç IP adresini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="f1ab2-157">INPUTOBJECT <IBlockchainIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="f1ab2-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f1ab2-158">`[BlockchainMemberName <String>]`: Blockzincirine üye adı.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="f1ab2-159">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="f1ab2-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f1ab2-160">`[Location <String>]`: Konum adı.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="f1ab2-161">`[OperationId <String>]`: İşlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="f1ab2-162">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f1ab2-163">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f1ab2-164">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="f1ab2-165">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="f1ab2-166">`[TransactionNodeName <String>]`: İşlem düğümü adı.</span><span class="sxs-lookup"><span data-stu-id="f1ab2-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="f1ab2-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1ab2-167">RELATED LINKS</span></span>

