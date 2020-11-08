---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276918"
---
# <span data-ttu-id="ff9ec-101">Update-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="ff9ec-101">Update-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="ff9ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="ff9ec-103">İşlem düğümünü güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-103">Update the transaction node.</span></span>

## <span data-ttu-id="ff9ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff9ec-104">SYNTAX</span></span>

### <span data-ttu-id="ff9ec-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ff9ec-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ff9ec-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="ff9ec-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ff9ec-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff9ec-107">DESCRIPTION</span></span>
<span data-ttu-id="ff9ec-108">İşlem düğümünü güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-108">Update the transaction node.</span></span>

## <span data-ttu-id="ff9ec-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff9ec-109">EXAMPLES</span></span>

### <span data-ttu-id="ff9ec-110">Örnek 1: bir transdüğümde güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ff9ec-110">Example 1: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="ff9ec-111">Bu komut, bir işlem düğümünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-111">This command updates a transaction node.</span></span>

### <span data-ttu-id="ff9ec-112">Örnek 2: bir transdüğüm düğümünü güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ff9ec-112">Example 2: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="ff9ec-113">Bu komut, bir işlem düğümünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-113">This command updates a transaction node.</span></span>

## <span data-ttu-id="ff9ec-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff9ec-114">PARAMETERS</span></span>

### <span data-ttu-id="ff9ec-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="ff9ec-115">-BlockchainMemberName</span></span>
<span data-ttu-id="ff9ec-116">Blockzincir üye adı.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="ff9ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff9ec-117">-DefaultProfile</span></span>
<span data-ttu-id="ff9ec-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff9ec-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="ff9ec-119">-FirewallRule</span></span>
<span data-ttu-id="ff9ec-120">Güvenlik duvarı kurallarını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="ff9ec-121">Oluşturmak için, FIREWALLRULE özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ff9ec-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff9ec-122">-InputObject</span></span>
<span data-ttu-id="ff9ec-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ff9ec-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="ff9ec-124">-Name</span></span>
<span data-ttu-id="ff9ec-125">İşlem düğümü adı.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9ec-126">-Parola</span><span class="sxs-lookup"><span data-stu-id="ff9ec-126">-Password</span></span>
<span data-ttu-id="ff9ec-127">İşlem düğümü DNS uç noktası temel kimlik doğrulama parolasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="ff9ec-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff9ec-128">-ResourceGroupName</span></span>
<span data-ttu-id="ff9ec-129">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ff9ec-130">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ff9ec-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ff9ec-131">-SubscriptionId</span></span>
<span data-ttu-id="ff9ec-132">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ff9ec-133">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ff9ec-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="ff9ec-134">-Confirm</span></span>
<span data-ttu-id="ff9ec-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff9ec-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff9ec-136">-WhatIf</span></span>
<span data-ttu-id="ff9ec-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff9ec-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff9ec-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff9ec-139">CommonParameters</span></span>
<span data-ttu-id="ff9ec-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff9ec-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff9ec-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff9ec-142">INPUTS</span></span>

### <span data-ttu-id="ff9ec-143">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. model. ıblockchainıdentity</span><span class="sxs-lookup"><span data-stu-id="ff9ec-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="ff9ec-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff9ec-144">OUTPUTS</span></span>

### <span data-ttu-id="ff9ec-145">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. ıctionnode</span><span class="sxs-lookup"><span data-stu-id="ff9ec-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="ff9ec-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff9ec-146">NOTES</span></span>

<span data-ttu-id="ff9ec-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="ff9ec-147">ALIASES</span></span>

<span data-ttu-id="ff9ec-148">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="ff9ec-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ff9ec-149">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ff9ec-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ff9ec-151">FIREWALLRULE <ıfirewallrule [] >: güvenlik duvarı kurallarını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-151">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="ff9ec-152">`[EndIPAddress <String>]`: Güvenlik duvarı kuralı aralığının bitiş IP adresini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-152">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="ff9ec-153">`[RuleName <String>]`: Güvenlik Duvarı kurallarının adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-153">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="ff9ec-154">`[StartIPAddress <String>]`: Güvenlik duvarı kuralı aralığının başlangıç IP adresini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-154">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="ff9ec-155">INPUTOBJECT <IBlockchainIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="ff9ec-155">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ff9ec-156">`[BlockchainMemberName <String>]`: Blockzincirine üye adı.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="ff9ec-157">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="ff9ec-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ff9ec-158">`[Location <String>]`: Konum adı.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-158">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="ff9ec-159">`[OperationId <String>]`: İşlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-159">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="ff9ec-160">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ff9ec-161">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ff9ec-162">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-162">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="ff9ec-163">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-163">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="ff9ec-164">`[TransactionNodeName <String>]`: İşlem düğümü adı.</span><span class="sxs-lookup"><span data-stu-id="ff9ec-164">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="ff9ec-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff9ec-165">RELATED LINKS</span></span>

