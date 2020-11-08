---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 3b660f5db14e1197c1e262a10f8225e4e9a82b81
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278400"
---
# <span data-ttu-id="15dd4-101">New-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="15dd4-101">New-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="15dd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15dd4-102">SYNOPSIS</span></span>
<span data-ttu-id="15dd4-103">Var olan bir sanal ağ kuralını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="15dd4-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="15dd4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15dd4-104">SYNTAX</span></span>

```
New-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="15dd4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15dd4-105">DESCRIPTION</span></span>
<span data-ttu-id="15dd4-106">Var olan bir sanal ağ kuralını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="15dd4-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="15dd4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15dd4-107">EXAMPLES</span></span>

### <span data-ttu-id="15dd4-108">Örnek 1: yeni bir MySql Server sanal ağ kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="15dd4-108">Example 1: Create a new MySql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> New-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="15dd4-109">Bu cmdlet 'ler bir MySql sunucusu sanal ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15dd4-109">These cmdlets create a MySql server Virtual Network Rule.</span></span>

## <span data-ttu-id="15dd4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15dd4-110">PARAMETERS</span></span>

### <span data-ttu-id="15dd4-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="15dd4-111">-AsJob</span></span>
<span data-ttu-id="15dd4-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="15dd4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="15dd4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15dd4-113">-DefaultProfile</span></span>
<span data-ttu-id="15dd4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15dd4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15dd4-115">-Ignoremissingvnetserviceendpoint</span><span class="sxs-lookup"><span data-stu-id="15dd4-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="15dd4-116">Sanal ağın VNET hizmeti uç noktası etkinleştirilmeden önce güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="15dd4-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="15dd4-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="15dd4-117">-Name</span></span>
<span data-ttu-id="15dd4-118">Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="15dd4-118">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15dd4-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="15dd4-119">-NoWait</span></span>
<span data-ttu-id="15dd4-120">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="15dd4-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="15dd4-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="15dd4-121">-PassThru</span></span>
<span data-ttu-id="15dd4-122">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="15dd4-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="15dd4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15dd4-123">-ResourceGroupName</span></span>
<span data-ttu-id="15dd4-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="15dd4-124">The name of the resource group.</span></span>
<span data-ttu-id="15dd4-125">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="15dd4-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="15dd4-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="15dd4-126">-ServerName</span></span>
<span data-ttu-id="15dd4-127">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="15dd4-127">The name of the server.</span></span>

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

### <span data-ttu-id="15dd4-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="15dd4-128">-SubnetId</span></span>
<span data-ttu-id="15dd4-129">Sanal ağ alt ağının ARM kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="15dd4-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="15dd4-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="15dd4-130">-SubscriptionId</span></span>
<span data-ttu-id="15dd4-131">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="15dd4-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="15dd4-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="15dd4-132">-Confirm</span></span>
<span data-ttu-id="15dd4-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="15dd4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15dd4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15dd4-134">-WhatIf</span></span>
<span data-ttu-id="15dd4-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="15dd4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15dd4-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="15dd4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15dd4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15dd4-137">CommonParameters</span></span>
<span data-ttu-id="15dd4-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15dd4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15dd4-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="15dd4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15dd4-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15dd4-140">INPUTS</span></span>

## <span data-ttu-id="15dd4-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15dd4-141">OUTPUTS</span></span>

### <span data-ttu-id="15dd4-142">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Api20171201. ıvirtualnetworkrule</span><span class="sxs-lookup"><span data-stu-id="15dd4-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="15dd4-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15dd4-143">NOTES</span></span>

<span data-ttu-id="15dd4-144">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="15dd4-144">ALIASES</span></span>

## <span data-ttu-id="15dd4-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15dd4-145">RELATED LINKS</span></span>

