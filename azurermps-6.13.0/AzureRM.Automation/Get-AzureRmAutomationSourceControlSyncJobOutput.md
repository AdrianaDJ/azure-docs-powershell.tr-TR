---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 59de6fa12ef3c6bd774f05fe55d31d74bb9efa13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763484"
---
# <span data-ttu-id="357b9-101">Get-AzureRmAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="357b9-101">Get-AzureRmAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="357b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="357b9-102">SYNOPSIS</span></span>
<span data-ttu-id="357b9-103">Bir Azure Otomasyonu kaynak denetimi eşitleme işinin çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="357b9-103">Gets the output of an Azure Automation source control sync job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="357b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="357b9-104">SYNTAX</span></span>

```
Get-AzureRmAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="357b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="357b9-105">DESCRIPTION</span></span>
<span data-ttu-id="357b9-106">**Get-Azurermautomationsourcecontrolsyncjoi Input** cmdlet 'ı bir Azure Otomasyonu kaynak denetimi eşitleme işinin çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="357b9-106">The **Get-AzureRmAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="357b9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="357b9-107">EXAMPLES</span></span>

### <span data-ttu-id="357b9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="357b9-108">Example 1</span></span>
<span data-ttu-id="357b9-109">Bu komut, kaynak denetimi için kimlik 08d6vseç/66-27b6-463C-beea-bc48a67asetat 15 ile kaynak denetimi eşitleme işinin çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="357b9-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJobOutput -ResourceGroupName "rg1" `
                                                        -AutomationAccountName "devAccount" `
                                                        -Name "VSTSNative"
                                                        -Id "08d6d266-27b6-463c-beea-bc48a67ace15" `
                                                        -Stream Output | ForEach-Object {$_.summary}

========================================================================================================

Azure Automation Source Control Public Preview.
Supported runbooks to sync: PowerShell Workflow, PowerShell Scripts, DSC Configurations, Graphical, and Python 2.
Setting AzureRmEnvironment.
Getting AzureRunAsConnection.
Logging in to Azure...
Source control information for syncing:
[RepoUrl = https://contoso.visualstudio.com/_git/GitDemo] [Branch  = master] [FolderPath = /]
Verifying url: https://fcontoso.visualstudio.com/_git/GitDemo
Connecting to VSTS...

Source Control Sync Summary:

2 files synced:
 - RunbookA.ps1
 - RunbookB.ps1

Failed to import runbook:
 - RunbookC.ps1

File is not a runbook:
 - README.md
 - text_file.txt

File size exceeds 1Mb:
 - RunbookD_GreatherThan1MB.ps1

Invalid runbook name:
 - RunbookZ_ĈĦŕĬŞ.ps1

========================================================================================================
```

## <span data-ttu-id="357b9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="357b9-110">PARAMETERS</span></span>

### <span data-ttu-id="357b9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="357b9-111">-AutomationAccountName</span></span>
<span data-ttu-id="357b9-112">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="357b9-112">The automation account name.</span></span>

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

### <span data-ttu-id="357b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="357b9-113">-DefaultProfile</span></span>
<span data-ttu-id="357b9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="357b9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="357b9-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="357b9-115">-JobId</span></span>
<span data-ttu-id="357b9-116">Kaynak denetimi eşitleme iş kimliği.</span><span class="sxs-lookup"><span data-stu-id="357b9-116">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="357b9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="357b9-117">-ResourceGroupName</span></span>
<span data-ttu-id="357b9-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="357b9-118">The resource group name.</span></span>

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

### <span data-ttu-id="357b9-119">-Sourcedenetimadı</span><span class="sxs-lookup"><span data-stu-id="357b9-119">-SourceControlName</span></span>
<span data-ttu-id="357b9-120">Kaynak denetimi adı.</span><span class="sxs-lookup"><span data-stu-id="357b9-120">The source control name.</span></span>

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

### <span data-ttu-id="357b9-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="357b9-121">-Stream</span></span>
<span data-ttu-id="357b9-122">Akış türü.</span><span class="sxs-lookup"><span data-stu-id="357b9-122">The stream type.</span></span>
<span data-ttu-id="357b9-123">Varsayılan olarak Any olur.</span><span class="sxs-lookup"><span data-stu-id="357b9-123">Defaults to Any.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Output, Error

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="357b9-124">-Streamıd</span><span class="sxs-lookup"><span data-stu-id="357b9-124">-StreamId</span></span>
<span data-ttu-id="357b9-125">Akış kimliği.</span><span class="sxs-lookup"><span data-stu-id="357b9-125">The stream id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlSyncJobStreamId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="357b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="357b9-126">CommonParameters</span></span>
<span data-ttu-id="357b9-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="357b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="357b9-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="357b9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="357b9-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="357b9-129">INPUTS</span></span>

### <span data-ttu-id="357b9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="357b9-130">System.String</span></span>

### <span data-ttu-id="357b9-131">System. Guid</span><span class="sxs-lookup"><span data-stu-id="357b9-131">System.Guid</span></span>

### <span data-ttu-id="357b9-132">Microsoft. Azure. Commands. Automation. Common. SourceControlSyncJobStreamType</span><span class="sxs-lookup"><span data-stu-id="357b9-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="357b9-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="357b9-133">OUTPUTS</span></span>

### <span data-ttu-id="357b9-134">Microsoft. Azure. Commands. Automation. model. SourceControlSyncJobStream</span><span class="sxs-lookup"><span data-stu-id="357b9-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="357b9-135">Microsoft. Azure. Commands. Automation. model. SourceControlSyncJobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="357b9-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="357b9-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="357b9-136">NOTES</span></span>

## <span data-ttu-id="357b9-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="357b9-137">RELATED LINKS</span></span>
