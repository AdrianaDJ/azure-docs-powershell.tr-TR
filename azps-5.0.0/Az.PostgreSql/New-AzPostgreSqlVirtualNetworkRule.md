---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: f617f853a8e9106ecb2d1268dfbe4e46a22efb45
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278496"
---
# <span data-ttu-id="29c77-101">New-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="29c77-101">New-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="29c77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29c77-102">SYNOPSIS</span></span>
<span data-ttu-id="29c77-103">Var olan bir sanal ağ kuralını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="29c77-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="29c77-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29c77-104">SYNTAX</span></span>

```
New-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="29c77-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="29c77-105">DESCRIPTION</span></span>
<span data-ttu-id="29c77-106">Var olan bir sanal ağ kuralını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="29c77-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="29c77-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29c77-107">EXAMPLES</span></span>

### <span data-ttu-id="29c77-108">Örnek 1: yeni bir PostgreSql Server sanal ağ kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="29c77-108">Example 1: Create a new PostgreSql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> New-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="29c77-109">Bu cmdlet 'ler bir PostgreSql Server sanal ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29c77-109">These cmdlets create a PostgreSql server Virtual Network Rule.</span></span>

## <span data-ttu-id="29c77-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29c77-110">PARAMETERS</span></span>

### <span data-ttu-id="29c77-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="29c77-111">-AsJob</span></span>
<span data-ttu-id="29c77-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="29c77-112">Run the command as a job</span></span>

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

### <span data-ttu-id="29c77-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c77-113">-DefaultProfile</span></span>
<span data-ttu-id="29c77-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="29c77-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29c77-115">-Ignoremissingvnetserviceendpoint</span><span class="sxs-lookup"><span data-stu-id="29c77-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="29c77-116">Sanal ağın VNET hizmeti uç noktası etkinleştirilmeden önce güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="29c77-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="29c77-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="29c77-117">-Name</span></span>
<span data-ttu-id="29c77-118">Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="29c77-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="29c77-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="29c77-119">-NoWait</span></span>
<span data-ttu-id="29c77-120">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="29c77-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="29c77-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="29c77-121">-PassThru</span></span>
<span data-ttu-id="29c77-122">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="29c77-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="29c77-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29c77-123">-ResourceGroupName</span></span>
<span data-ttu-id="29c77-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="29c77-124">The name of the resource group.</span></span>
<span data-ttu-id="29c77-125">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="29c77-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="29c77-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="29c77-126">-ServerName</span></span>
<span data-ttu-id="29c77-127">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="29c77-127">The name of the server.</span></span>

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

### <span data-ttu-id="29c77-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="29c77-128">-SubnetId</span></span>
<span data-ttu-id="29c77-129">Sanal ağ alt ağının ARM kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="29c77-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="29c77-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="29c77-130">-SubscriptionId</span></span>
<span data-ttu-id="29c77-131">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="29c77-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="29c77-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="29c77-132">-Confirm</span></span>
<span data-ttu-id="29c77-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="29c77-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29c77-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29c77-134">-WhatIf</span></span>
<span data-ttu-id="29c77-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="29c77-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29c77-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="29c77-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29c77-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c77-137">CommonParameters</span></span>
<span data-ttu-id="29c77-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29c77-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c77-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="29c77-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c77-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29c77-140">INPUTS</span></span>

## <span data-ttu-id="29c77-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29c77-141">OUTPUTS</span></span>

### <span data-ttu-id="29c77-142">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. Api20171201. ıvirtualnetworkrule</span><span class="sxs-lookup"><span data-stu-id="29c77-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="29c77-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29c77-143">NOTES</span></span>

<span data-ttu-id="29c77-144">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="29c77-144">ALIASES</span></span>

## <span data-ttu-id="29c77-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29c77-145">RELATED LINKS</span></span>

