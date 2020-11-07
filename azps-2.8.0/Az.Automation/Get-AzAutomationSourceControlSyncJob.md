---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 8fa14eef62ac0e8a296349ff3a47cd67086bc3ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753300"
---
# <span data-ttu-id="06a2d-101">Get-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="06a2d-101">Get-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="06a2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="06a2d-103">Azure Otomasyonu kaynak denetimi eşitleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="06a2d-103">Gets Azure Automation source control sync jobs.</span></span>

## <span data-ttu-id="06a2d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06a2d-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06a2d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="06a2d-105">DESCRIPTION</span></span>
<span data-ttu-id="06a2d-106">Get-AzAutomationSourceControlSyncJob cmdlet 'i Azure Otomasyonu kaynak denetimi eşitleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="06a2d-106">The Get-AzAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="06a2d-107">Belirli bir kaynak denetimi eşitleme işine ulaşmak için, kimliğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="06a2d-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="06a2d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06a2d-108">EXAMPLES</span></span>

### <span data-ttu-id="06a2d-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="06a2d-109">Example 1</span></span>
<span data-ttu-id="06a2d-110">Bu komut, kaynak denetimi için tüm otomasyon kaynak denetimi eşitleme işlerini VSTSNative ile alır.</span><span class="sxs-lookup"><span data-stu-id="06a2d-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="06a2d-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="06a2d-111">Example 2</span></span>
<span data-ttu-id="06a2d-112">Bu komut, kaynak denetimi için kimlik 08d6vseç/66-27b6-463C-beea-bc48a67asetat 15 ile kaynak denetimi eşitleme işini alır.</span><span class="sxs-lookup"><span data-stu-id="06a2d-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"
                                                  -Id "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

## <span data-ttu-id="06a2d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06a2d-113">PARAMETERS</span></span>

### <span data-ttu-id="06a2d-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="06a2d-114">-AutomationAccountName</span></span>
<span data-ttu-id="06a2d-115">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="06a2d-115">The automation account name.</span></span>

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

### <span data-ttu-id="06a2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a2d-116">-DefaultProfile</span></span>
<span data-ttu-id="06a2d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06a2d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a2d-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="06a2d-118">-JobId</span></span>
<span data-ttu-id="06a2d-119">Kaynak denetimi eşitleme iş kimliği.</span><span class="sxs-lookup"><span data-stu-id="06a2d-119">The source control sync job id.</span></span>

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

### <span data-ttu-id="06a2d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06a2d-120">-ResourceGroupName</span></span>
<span data-ttu-id="06a2d-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="06a2d-121">The resource group name.</span></span>

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

### <span data-ttu-id="06a2d-122">-Sourcedenetimadı</span><span class="sxs-lookup"><span data-stu-id="06a2d-122">-SourceControlName</span></span>
<span data-ttu-id="06a2d-123">İşin kaynak denetimi adı.</span><span class="sxs-lookup"><span data-stu-id="06a2d-123">The source control name of the job.</span></span>

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

### <span data-ttu-id="06a2d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a2d-124">CommonParameters</span></span>
<span data-ttu-id="06a2d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06a2d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a2d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06a2d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a2d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06a2d-127">INPUTS</span></span>

### <span data-ttu-id="06a2d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="06a2d-128">System.String</span></span>

### <span data-ttu-id="06a2d-129">System. Guid</span><span class="sxs-lookup"><span data-stu-id="06a2d-129">System.Guid</span></span>

## <span data-ttu-id="06a2d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06a2d-130">OUTPUTS</span></span>

### <span data-ttu-id="06a2d-131">Microsoft. Azure. Commands. Automation. model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="06a2d-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="06a2d-132">Microsoft. Azure. Commands. Automation. model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="06a2d-132">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="06a2d-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06a2d-133">NOTES</span></span>

## <span data-ttu-id="06a2d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06a2d-134">RELATED LINKS</span></span>
