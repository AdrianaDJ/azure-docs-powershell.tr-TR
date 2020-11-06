---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationSourceControlSyncJob.md
ms.openlocfilehash: 4a5864e9572a21442a5333232fe5f705fb1b5687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572957"
---
# <span data-ttu-id="9d0b0-101">Start-AzureRmAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="9d0b0-101">Start-AzureRmAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="9d0b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d0b0-102">SYNOPSIS</span></span>
<span data-ttu-id="9d0b0-103">Azure Otomasyonu kaynak denetimi eşitleme işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="9d0b0-103">Starts an Azure Automation source control sync job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d0b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d0b0-104">SYNTAX</span></span>

```
Start-AzureRmAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d0b0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d0b0-105">DESCRIPTION</span></span>
<span data-ttu-id="9d0b0-106">Start-AzureRmAutomationSourceControlSyncJob cmdlet, verilen kaynak denetimi adı için bir Azure Otomasyonu kaynak örneği denetim eşitleme işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="9d0b0-106">The Start-AzureRmAutomationSourceControlSyncJob cmdlet starts a Azure Automation souce control sync job for the given source control name.</span></span>

## <span data-ttu-id="9d0b0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d0b0-107">EXAMPLES</span></span>

### <span data-ttu-id="9d0b0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9d0b0-108">Example 1</span></span>
```powershell
PS C:\> Start-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="9d0b0-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d0b0-109">PARAMETERS</span></span>

### <span data-ttu-id="9d0b0-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9d0b0-110">-AutomationAccountName</span></span>
<span data-ttu-id="9d0b0-111">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="9d0b0-111">The automation account name.</span></span>

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

### <span data-ttu-id="9d0b0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d0b0-112">-DefaultProfile</span></span>
<span data-ttu-id="9d0b0-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9d0b0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d0b0-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="9d0b0-114">-JobId</span></span>
<span data-ttu-id="9d0b0-115">Kaynak denetimi eşitleme iş kimliği.</span><span class="sxs-lookup"><span data-stu-id="9d0b0-115">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d0b0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d0b0-116">-ResourceGroupName</span></span>
<span data-ttu-id="9d0b0-117">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9d0b0-117">The resource group name.</span></span>

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

### <span data-ttu-id="9d0b0-118">-Sourcedenetimadı</span><span class="sxs-lookup"><span data-stu-id="9d0b0-118">-SourceControlName</span></span>
<span data-ttu-id="9d0b0-119">Kaynak denetimi adı.</span><span class="sxs-lookup"><span data-stu-id="9d0b0-119">The source control name.</span></span>

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

### <span data-ttu-id="9d0b0-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="9d0b0-120">-Confirm</span></span>
<span data-ttu-id="9d0b0-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9d0b0-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d0b0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d0b0-122">-WhatIf</span></span>
<span data-ttu-id="9d0b0-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9d0b0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d0b0-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9d0b0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d0b0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d0b0-125">CommonParameters</span></span>
<span data-ttu-id="9d0b0-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d0b0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d0b0-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d0b0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d0b0-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d0b0-128">INPUTS</span></span>

### <span data-ttu-id="9d0b0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9d0b0-129">System.String</span></span>

## <span data-ttu-id="9d0b0-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d0b0-130">OUTPUTS</span></span>

### <span data-ttu-id="9d0b0-131">Microsoft. Azure. Commands. Automation. model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="9d0b0-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="9d0b0-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d0b0-132">NOTES</span></span>

## <span data-ttu-id="9d0b0-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d0b0-133">RELATED LINKS</span></span>
