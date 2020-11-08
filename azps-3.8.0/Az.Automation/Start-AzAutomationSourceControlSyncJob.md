---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 1f685307ae1d6f9a030ac5c242af9fcec97c032b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096047"
---
# <span data-ttu-id="5a9e1-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="5a9e1-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="5a9e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a9e1-102">SYNOPSIS</span></span>
<span data-ttu-id="5a9e1-103">Azure Otomasyonu kaynak denetimi eşitleme işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="5a9e1-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="5a9e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a9e1-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a9e1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a9e1-105">DESCRIPTION</span></span>
<span data-ttu-id="5a9e1-106">Start-AzAutomationSourceControlSyncJob cmdlet, verilen kaynak denetimi adı için bir Azure Otomasyonu kaynak denetimi eşitleme işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="5a9e1-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="5a9e1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a9e1-107">EXAMPLES</span></span>

### <span data-ttu-id="5a9e1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5a9e1-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="5a9e1-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a9e1-109">PARAMETERS</span></span>

### <span data-ttu-id="5a9e1-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5a9e1-110">-AutomationAccountName</span></span>
<span data-ttu-id="5a9e1-111">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="5a9e1-111">The automation account name.</span></span>

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

### <span data-ttu-id="5a9e1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a9e1-112">-DefaultProfile</span></span>
<span data-ttu-id="5a9e1-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a9e1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a9e1-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="5a9e1-114">-JobId</span></span>
<span data-ttu-id="5a9e1-115">Kaynak denetimi eşitleme iş kimliği.</span><span class="sxs-lookup"><span data-stu-id="5a9e1-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="5a9e1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a9e1-116">-ResourceGroupName</span></span>
<span data-ttu-id="5a9e1-117">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5a9e1-117">The resource group name.</span></span>

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

### <span data-ttu-id="5a9e1-118">-Sourcedenetimadı</span><span class="sxs-lookup"><span data-stu-id="5a9e1-118">-SourceControlName</span></span>
<span data-ttu-id="5a9e1-119">Kaynak denetimi adı.</span><span class="sxs-lookup"><span data-stu-id="5a9e1-119">The source control name.</span></span>

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

### <span data-ttu-id="5a9e1-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="5a9e1-120">-Confirm</span></span>
<span data-ttu-id="5a9e1-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5a9e1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a9e1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a9e1-122">-WhatIf</span></span>
<span data-ttu-id="5a9e1-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5a9e1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a9e1-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5a9e1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a9e1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a9e1-125">CommonParameters</span></span>
<span data-ttu-id="5a9e1-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a9e1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a9e1-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a9e1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a9e1-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a9e1-128">INPUTS</span></span>

### <span data-ttu-id="5a9e1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5a9e1-129">System.String</span></span>

## <span data-ttu-id="5a9e1-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a9e1-130">OUTPUTS</span></span>

### <span data-ttu-id="5a9e1-131">Microsoft. Azure. Commands. Automation. model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="5a9e1-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="5a9e1-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a9e1-132">NOTES</span></span>

## <span data-ttu-id="5a9e1-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a9e1-133">RELATED LINKS</span></span>