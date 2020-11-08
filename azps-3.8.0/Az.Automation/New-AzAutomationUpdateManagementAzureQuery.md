---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationupdatemanagementazurequery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
ms.openlocfilehash: 68139ff184df62583b3077a38fbc2e26fd5eae09
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104953"
---
# <span data-ttu-id="25777-101">New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="25777-101">New-AzAutomationUpdateManagementAzureQuery</span></span>

## <span data-ttu-id="25777-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25777-102">SYNOPSIS</span></span>
<span data-ttu-id="25777-103">Azure Otomasyonu yazılım güncelleştirme yapılandırması Azure sorgu nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="25777-103">Creates azure automation software update configuration azure query object.</span></span>

## <span data-ttu-id="25777-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25777-104">SYNTAX</span></span>

```
New-AzAutomationUpdateManagementAzureQuery -Scope <String[]> [-Location <String[]>] [-Tag <Hashtable>]
 [-FilterOperator <TagOperators>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25777-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="25777-105">DESCRIPTION</span></span>
<span data-ttu-id="25777-106">Dinamik olarak çözümlenen Azure sanal makinelerin listesini güncelleştirmek için bir zamanlamada çalışacak bir yazılım güncelleştirme yapılandırması oluşturmak için kullanılacak bir yazılım güncelleştirme yapılandırması Azure sorguları nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="25777-106">Creates a software update configuration azure queries object that will be used to create a software update configuration which will runs on a schedule to update a list of dynamically resolved list of azure virtual machines.</span></span>

## <span data-ttu-id="25777-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25777-107">EXAMPLES</span></span>

### <span data-ttu-id="25777-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="25777-108">Example 1</span></span>
```powershell
PS C:\>$query1Scope = @(        
"/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/resourceGroupName",
"/subscriptions/32e2445a-0984-4fa5-86a4-0280d76c4b2d/"
    )
PS C:\>$query1Location =@("Japan East", "UK South")
PS C:\>$query1FilterOperator = "All"
PS C:\>$tag1 = @{"tag1"= @("tag1Value1", "tag1Value2")}
PS C:\>$tag1.add("tag2", "tag2Value")
PS C:\>$azq = New-AzAutomationUpdateManagementAzureQuery -ResourceGroupName "mygroup" `
                                       -AutomationAccountName "myaccount" `
                                       -Scope $query1Scope `
                                       -Location $query1Location `
                                       -Tag $tag1
PS C:\>$AzureQueries = @($azq)
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"

PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `                                                 
                                                 -AzureQuery $AzureQueries `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :

```

## <span data-ttu-id="25777-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25777-109">PARAMETERS</span></span>

### <span data-ttu-id="25777-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="25777-110">-AutomationAccountName</span></span>
<span data-ttu-id="25777-111">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="25777-111">The automation account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25777-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25777-112">-DefaultProfile</span></span>
<span data-ttu-id="25777-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25777-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25777-114">-FilterOperator</span><span class="sxs-lookup"><span data-stu-id="25777-114">-FilterOperator</span></span>
<span data-ttu-id="25777-115">Etiket Filtresi işleci.</span><span class="sxs-lookup"><span data-stu-id="25777-115">Tag filter operator.</span></span>

```yaml
Type: TagOperators
Parameter Sets: (All)
Aliases:
Accepted values: All, Any

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="25777-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="25777-116">-Location</span></span>
<span data-ttu-id="25777-117">Azure sanal makinelerinin konumlarının listesi.</span><span class="sxs-lookup"><span data-stu-id="25777-117">List of locations for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="25777-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25777-118">-ResourceGroupName</span></span>
<span data-ttu-id="25777-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="25777-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25777-120">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="25777-120">-Scope</span></span>
<span data-ttu-id="25777-121">Azure sanal makinelerinin kaynak kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="25777-121">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="25777-122">Etiketli</span><span class="sxs-lookup"><span data-stu-id="25777-122">-Tag</span></span>
<span data-ttu-id="25777-123">Azure sanal makinelerinin etiketi.</span><span class="sxs-lookup"><span data-stu-id="25777-123">Tag for azure virtual machines.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="25777-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25777-124">CommonParameters</span></span>
<span data-ttu-id="25777-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25777-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="25777-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25777-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25777-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25777-127">INPUTS</span></span>

### <span data-ttu-id="25777-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="25777-128">System.String[]</span></span>

### <span data-ttu-id="25777-129">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="25777-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="25777-130">Microsoft. Azure. Commands. Automation. model. UpdateManagement. TagOperators</span><span class="sxs-lookup"><span data-stu-id="25777-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span></span>

### <span data-ttu-id="25777-131">System. String</span><span class="sxs-lookup"><span data-stu-id="25777-131">System.String</span></span>

## <span data-ttu-id="25777-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25777-132">OUTPUTS</span></span>

### <span data-ttu-id="25777-133">Microsoft. Azure. Commands. Automation. model. UpdateManagement. Azuyeniden sorgulama</span><span class="sxs-lookup"><span data-stu-id="25777-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span></span>

## <span data-ttu-id="25777-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25777-134">NOTES</span></span>

## <span data-ttu-id="25777-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25777-135">RELATED LINKS</span></span>
