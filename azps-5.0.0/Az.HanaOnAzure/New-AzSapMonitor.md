---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: 95a9e996612827b355b141165231651e17c78f6d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275343"
---
# <span data-ttu-id="54233-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="54233-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="54233-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54233-102">SYNOPSIS</span></span>
<span data-ttu-id="54233-103">Belirtilen abonelik, kaynak grubu ve kaynak adı için bir SAP izlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54233-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="54233-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54233-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="54233-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="54233-105">DESCRIPTION</span></span>
<span data-ttu-id="54233-106">Belirtilen abonelik, kaynak grubu ve kaynak adı için bir SAP izlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54233-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="54233-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54233-107">EXAMPLES</span></span>

### <span data-ttu-id="54233-108">Örnek 1: yeni SAP monitörü</span><span class="sxs-lookup"><span data-stu-id="54233-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="54233-109">Bu komut bir SAP monitörü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54233-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="54233-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54233-110">PARAMETERS</span></span>

### <span data-ttu-id="54233-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="54233-111">-AsJob</span></span>
<span data-ttu-id="54233-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="54233-112">Run the command as a job</span></span>

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

### <span data-ttu-id="54233-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54233-113">-DefaultProfile</span></span>
<span data-ttu-id="54233-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54233-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54233-115">-Enablecustomeranalitik</span><span class="sxs-lookup"><span data-stu-id="54233-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="54233-116">Microsoft 'a analitik gönderilip gönderilmeyeceğini gösteren değer</span><span class="sxs-lookup"><span data-stu-id="54233-116">The value indicating whether to send analytics to Microsoft</span></span>

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

### <span data-ttu-id="54233-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="54233-117">-Location</span></span>
<span data-ttu-id="54233-118">Kaynağın yaşadığı coğrafi konum</span><span class="sxs-lookup"><span data-stu-id="54233-118">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="54233-119">-Loganalyzer Tics</span><span class="sxs-lookup"><span data-stu-id="54233-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="54233-120">İzleme için kullanılacak Log Analytics çalışma alanının çalışma alanı KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="54233-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

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

### <span data-ttu-id="54233-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="54233-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="54233-122">İzleme için kullanılan Log Analytics çalışma alanının ARM KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="54233-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="54233-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="54233-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="54233-124">İzleme için kullanılan Log Analytics çalışma alanının paylaşılan anahtarı</span><span class="sxs-lookup"><span data-stu-id="54233-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="54233-125">-Monitorsubnetresourceıd</span><span class="sxs-lookup"><span data-stu-id="54233-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="54233-126">SAP izlemenin dağıtılacağı alt ağ.</span><span class="sxs-lookup"><span data-stu-id="54233-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="54233-127">Bu, HANA veritabanının aynı alt ağıyla olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="54233-127">It should be the same subnet of HANA database.</span></span>

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

### <span data-ttu-id="54233-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="54233-128">-Name</span></span>
<span data-ttu-id="54233-129">SAP izleyici kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="54233-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="54233-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="54233-130">-NoWait</span></span>
<span data-ttu-id="54233-131">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="54233-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="54233-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54233-132">-ResourceGroupName</span></span>
<span data-ttu-id="54233-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="54233-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="54233-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="54233-134">-SubscriptionId</span></span>
<span data-ttu-id="54233-135">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="54233-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="54233-136">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="54233-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="54233-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="54233-137">-Tag</span></span>
<span data-ttu-id="54233-138">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="54233-138">Resource tags.</span></span>

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

### <span data-ttu-id="54233-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="54233-139">-Confirm</span></span>
<span data-ttu-id="54233-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="54233-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54233-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54233-141">-WhatIf</span></span>
<span data-ttu-id="54233-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="54233-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54233-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="54233-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54233-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54233-144">CommonParameters</span></span>
<span data-ttu-id="54233-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54233-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54233-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="54233-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54233-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54233-147">INPUTS</span></span>

## <span data-ttu-id="54233-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54233-148">OUTPUTS</span></span>

### <span data-ttu-id="54233-149">Microsoft. Azure. PowerShell. cmdlet. Hana</span><span class="sxs-lookup"><span data-stu-id="54233-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="54233-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54233-150">NOTES</span></span>

<span data-ttu-id="54233-151">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="54233-151">ALIASES</span></span>

## <span data-ttu-id="54233-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54233-152">RELATED LINKS</span></span>

