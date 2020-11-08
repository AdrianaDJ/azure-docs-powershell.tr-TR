---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: 95a9e996612827b355b141165231651e17c78f6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274517"
---
# <span data-ttu-id="3eed5-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="3eed5-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="3eed5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eed5-102">SYNOPSIS</span></span>
<span data-ttu-id="3eed5-103">Belirtilen abonelik, kaynak grubu ve kaynak adı için bir SAP izlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3eed5-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="3eed5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3eed5-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3eed5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3eed5-105">DESCRIPTION</span></span>
<span data-ttu-id="3eed5-106">Belirtilen abonelik, kaynak grubu ve kaynak adı için bir SAP izlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3eed5-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="3eed5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3eed5-107">EXAMPLES</span></span>

### <span data-ttu-id="3eed5-108">Örnek 1: yeni SAP monitörü</span><span class="sxs-lookup"><span data-stu-id="3eed5-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="3eed5-109">Bu komut bir SAP monitörü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3eed5-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="3eed5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3eed5-110">PARAMETERS</span></span>

### <span data-ttu-id="3eed5-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="3eed5-111">-AsJob</span></span>
<span data-ttu-id="3eed5-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="3eed5-112">Run the command as a job</span></span>

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

### <span data-ttu-id="3eed5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eed5-113">-DefaultProfile</span></span>
<span data-ttu-id="3eed5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3eed5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3eed5-115">-Enablecustomeranalitik</span><span class="sxs-lookup"><span data-stu-id="3eed5-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="3eed5-116">Microsoft 'a analitik gönderilip gönderilmeyeceğini gösteren değer</span><span class="sxs-lookup"><span data-stu-id="3eed5-116">The value indicating whether to send analytics to Microsoft</span></span>

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

### <span data-ttu-id="3eed5-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="3eed5-117">-Location</span></span>
<span data-ttu-id="3eed5-118">Kaynağın yaşadığı coğrafi konum</span><span class="sxs-lookup"><span data-stu-id="3eed5-118">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="3eed5-119">-Loganalyzer Tics</span><span class="sxs-lookup"><span data-stu-id="3eed5-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="3eed5-120">İzleme için kullanılacak Log Analytics çalışma alanının çalışma alanı KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="3eed5-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

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

### <span data-ttu-id="3eed5-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="3eed5-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="3eed5-122">İzleme için kullanılan Log Analytics çalışma alanının ARM KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="3eed5-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="3eed5-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="3eed5-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="3eed5-124">İzleme için kullanılan Log Analytics çalışma alanının paylaşılan anahtarı</span><span class="sxs-lookup"><span data-stu-id="3eed5-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="3eed5-125">-Monitorsubnetresourceıd</span><span class="sxs-lookup"><span data-stu-id="3eed5-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="3eed5-126">SAP izlemenin dağıtılacağı alt ağ.</span><span class="sxs-lookup"><span data-stu-id="3eed5-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="3eed5-127">Bu, HANA veritabanının aynı alt ağıyla olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3eed5-127">It should be the same subnet of HANA database.</span></span>

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

### <span data-ttu-id="3eed5-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="3eed5-128">-Name</span></span>
<span data-ttu-id="3eed5-129">SAP izleyici kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="3eed5-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eed5-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3eed5-130">-NoWait</span></span>
<span data-ttu-id="3eed5-131">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="3eed5-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3eed5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eed5-132">-ResourceGroupName</span></span>
<span data-ttu-id="3eed5-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3eed5-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="3eed5-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="3eed5-134">-SubscriptionId</span></span>
<span data-ttu-id="3eed5-135">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3eed5-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3eed5-136">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3eed5-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3eed5-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3eed5-137">-Tag</span></span>
<span data-ttu-id="3eed5-138">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="3eed5-138">Resource tags.</span></span>

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

### <span data-ttu-id="3eed5-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="3eed5-139">-Confirm</span></span>
<span data-ttu-id="3eed5-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3eed5-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eed5-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eed5-141">-WhatIf</span></span>
<span data-ttu-id="3eed5-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3eed5-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eed5-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3eed5-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eed5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eed5-144">CommonParameters</span></span>
<span data-ttu-id="3eed5-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3eed5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eed5-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3eed5-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eed5-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3eed5-147">INPUTS</span></span>

## <span data-ttu-id="3eed5-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3eed5-148">OUTPUTS</span></span>

### <span data-ttu-id="3eed5-149">Microsoft. Azure. PowerShell. cmdlet. Hana</span><span class="sxs-lookup"><span data-stu-id="3eed5-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="3eed5-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3eed5-150">NOTES</span></span>

<span data-ttu-id="3eed5-151">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="3eed5-151">ALIASES</span></span>

## <span data-ttu-id="3eed5-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3eed5-152">RELATED LINKS</span></span>

