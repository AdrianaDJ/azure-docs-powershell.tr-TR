---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: c5b5e761306c37e67f6b6a2398a5985872722efa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279542"
---
# <span data-ttu-id="e9e06-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="e9e06-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="e9e06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9e06-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e06-103">İşlem düğümünü oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="e9e06-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="e9e06-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9e06-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e9e06-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9e06-105">DESCRIPTION</span></span>
<span data-ttu-id="e9e06-106">İşlem düğümünü oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="e9e06-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="e9e06-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9e06-107">EXAMPLES</span></span>

### <span data-ttu-id="e9e06-108">Örnek 1: blockzincirlem düğümü oluşturma</span><span class="sxs-lookup"><span data-stu-id="e9e06-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="e9e06-109">Bu komut bir blockzincirine Transaction düğümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9e06-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="e9e06-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9e06-110">PARAMETERS</span></span>

### <span data-ttu-id="e9e06-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="e9e06-111">-AsJob</span></span>
<span data-ttu-id="e9e06-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="e9e06-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e9e06-113">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="e9e06-113">-BlockchainMemberName</span></span>
<span data-ttu-id="e9e06-114">Blockzincir üye adı.</span><span class="sxs-lookup"><span data-stu-id="e9e06-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="e9e06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e06-115">-DefaultProfile</span></span>
<span data-ttu-id="e9e06-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e9e06-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9e06-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="e9e06-117">-FirewallRule</span></span>
<span data-ttu-id="e9e06-118">Güvenlik duvarı kurallarını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e9e06-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="e9e06-119">Oluşturmak için, FIREWALLRULE özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e9e06-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e9e06-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="e9e06-120">-Location</span></span>
<span data-ttu-id="e9e06-121">İşlem düğümü konumunu alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e9e06-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="e9e06-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="e9e06-122">-Name</span></span>
<span data-ttu-id="e9e06-123">İşlem düğümü adı.</span><span class="sxs-lookup"><span data-stu-id="e9e06-123">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9e06-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e9e06-124">-NoWait</span></span>
<span data-ttu-id="e9e06-125">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="e9e06-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e9e06-126">-Parola</span><span class="sxs-lookup"><span data-stu-id="e9e06-126">-Password</span></span>
<span data-ttu-id="e9e06-127">İşlem düğümü DNS uç noktası temel kimlik doğrulama parolasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e9e06-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="e9e06-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9e06-128">-ResourceGroupName</span></span>
<span data-ttu-id="e9e06-129">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e9e06-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e9e06-130">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9e06-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e9e06-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="e9e06-131">-SubscriptionId</span></span>
<span data-ttu-id="e9e06-132">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="e9e06-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e9e06-133">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="e9e06-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e9e06-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="e9e06-134">-Confirm</span></span>
<span data-ttu-id="e9e06-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e9e06-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9e06-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9e06-136">-WhatIf</span></span>
<span data-ttu-id="e9e06-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9e06-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9e06-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e9e06-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9e06-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e06-139">CommonParameters</span></span>
<span data-ttu-id="e9e06-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9e06-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e06-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e9e06-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e06-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9e06-142">INPUTS</span></span>

## <span data-ttu-id="e9e06-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9e06-143">OUTPUTS</span></span>

### <span data-ttu-id="e9e06-144">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. ıctionnode</span><span class="sxs-lookup"><span data-stu-id="e9e06-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="e9e06-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9e06-145">NOTES</span></span>

<span data-ttu-id="e9e06-146">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="e9e06-146">ALIASES</span></span>

<span data-ttu-id="e9e06-147">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="e9e06-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e9e06-148">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e9e06-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e9e06-149">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e9e06-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e9e06-150">FIREWALLRULE <ıfirewallrule [] >: güvenlik duvarı kurallarını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e9e06-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="e9e06-151">`[EndIPAddress <String>]`: Güvenlik duvarı kuralı aralığının bitiş IP adresini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e9e06-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="e9e06-152">`[RuleName <String>]`: Güvenlik Duvarı kurallarının adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e9e06-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="e9e06-153">`[StartIPAddress <String>]`: Güvenlik duvarı kuralı aralığının başlangıç IP adresini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e9e06-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="e9e06-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9e06-154">RELATED LINKS</span></span>

