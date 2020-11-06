---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJob.md
ms.openlocfilehash: 213df264e4ecd458c8505d521556f49265577333
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592807"
---
# <span data-ttu-id="cf7b9-101">Get-AzureRmAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="cf7b9-101">Get-AzureRmAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="cf7b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf7b9-102">SYNOPSIS</span></span>
<span data-ttu-id="cf7b9-103">Azure Otomasyonu kaynak denetimi eşitleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="cf7b9-103">Gets Azure Automation source control sync jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf7b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf7b9-104">SYNTAX</span></span>

```
Get-AzureRmAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf7b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf7b9-105">DESCRIPTION</span></span>
<span data-ttu-id="cf7b9-106">Get-AzureRmAutomationSourceControlSyncJob cmdlet 'i Azure Otomasyonu kaynak denetimi eşitleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="cf7b9-106">The Get-AzureRmAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="cf7b9-107">Belirli bir kaynak denetimi eşitleme işine ulaşmak için, kimliğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="cf7b9-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="cf7b9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf7b9-108">EXAMPLES</span></span>

### <span data-ttu-id="cf7b9-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cf7b9-109">Example 1</span></span>
<span data-ttu-id="cf7b9-110">Bu komut, kaynak denetimi için tüm otomasyon kaynak denetimi eşitleme işlerini VSTSNative ile alır.</span><span class="sxs-lookup"><span data-stu-id="cf7b9-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="cf7b9-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cf7b9-111">Example 2</span></span>
<span data-ttu-id="cf7b9-112">Bu komut, kaynak denetimi için kimlik 08d6vseç/66-27b6-463C-beea-bc48a67asetat 15 ile kaynak denetimi eşitleme işini alır.</span><span class="sxs-lookup"><span data-stu-id="cf7b9-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"
                                                  -Id "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

## <span data-ttu-id="cf7b9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf7b9-113">PARAMETERS</span></span>

### <span data-ttu-id="cf7b9-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cf7b9-114">-AutomationAccountName</span></span>
<span data-ttu-id="cf7b9-115">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="cf7b9-115">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf7b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf7b9-116">-DefaultProfile</span></span>
<span data-ttu-id="cf7b9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cf7b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf7b9-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="cf7b9-118">-JobId</span></span>
<span data-ttu-id="cf7b9-119">Kaynak denetimi eşitleme iş kimliği.</span><span class="sxs-lookup"><span data-stu-id="cf7b9-119">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf7b9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf7b9-120">-ResourceGroupName</span></span>
<span data-ttu-id="cf7b9-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cf7b9-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf7b9-122">-Sourcedenetimadı</span><span class="sxs-lookup"><span data-stu-id="cf7b9-122">-SourceControlName</span></span>
<span data-ttu-id="cf7b9-123">İşin kaynak denetimi adı.</span><span class="sxs-lookup"><span data-stu-id="cf7b9-123">The source control name of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf7b9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf7b9-124">CommonParameters</span></span>
<span data-ttu-id="cf7b9-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf7b9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf7b9-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf7b9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf7b9-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf7b9-127">INPUTS</span></span>

### <span data-ttu-id="cf7b9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cf7b9-128">System.String</span></span>

### <span data-ttu-id="cf7b9-129">System. Guid</span><span class="sxs-lookup"><span data-stu-id="cf7b9-129">System.Guid</span></span>

## <span data-ttu-id="cf7b9-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf7b9-130">OUTPUTS</span></span>

### <span data-ttu-id="cf7b9-131">Microsoft. Azure. Commands. Automation. model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="cf7b9-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="cf7b9-132">Microsoft. Azure. Commands. Automation. model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="cf7b9-132">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="cf7b9-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf7b9-133">NOTES</span></span>

## <span data-ttu-id="cf7b9-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf7b9-134">RELATED LINKS</span></span>
