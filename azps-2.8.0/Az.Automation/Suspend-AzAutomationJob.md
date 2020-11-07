---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 850ff932bdae35bd21ab83c745b5da8c056d778d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753193"
---
# <span data-ttu-id="3d4cf-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3d4cf-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="3d4cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d4cf-102">SYNOPSIS</span></span>
<span data-ttu-id="3d4cf-103">Otomasyon işini askıya alır.</span><span class="sxs-lookup"><span data-stu-id="3d4cf-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="3d4cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d4cf-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d4cf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d4cf-105">DESCRIPTION</span></span>
<span data-ttu-id="3d4cf-106">**Askıya al-AzAutomationJob** cmdlet 'ı bir Azure Otomasyonu işini askıya alır.</span><span class="sxs-lookup"><span data-stu-id="3d4cf-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="3d4cf-107">Çalışan bir Otomasyon işi belirtin.</span><span class="sxs-lookup"><span data-stu-id="3d4cf-107">Specify a running Automation job.</span></span>
<span data-ttu-id="3d4cf-108">Askıya alınmış bir işi sürdürmek için Resume-AzAutomationJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3d4cf-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="3d4cf-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d4cf-109">EXAMPLES</span></span>

### <span data-ttu-id="3d4cf-110">Örnek 1: işi askıya alma</span><span class="sxs-lookup"><span data-stu-id="3d4cf-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3d4cf-111">Bu komut belirtilen KIMLIĞE sahip işi askıya alır.</span><span class="sxs-lookup"><span data-stu-id="3d4cf-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="3d4cf-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d4cf-112">PARAMETERS</span></span>

### <span data-ttu-id="3d4cf-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3d4cf-113">-AutomationAccountName</span></span>
<span data-ttu-id="3d4cf-114">Bu cmdlet 'in işi askıya aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d4cf-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="3d4cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d4cf-115">-DefaultProfile</span></span>
<span data-ttu-id="3d4cf-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3d4cf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d4cf-117">-ID</span><span class="sxs-lookup"><span data-stu-id="3d4cf-117">-Id</span></span>
<span data-ttu-id="3d4cf-118">Bu cmdlet 'in askıya aldığı bir işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d4cf-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d4cf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d4cf-119">-ResourceGroupName</span></span>
<span data-ttu-id="3d4cf-120">Bu cmdlet 'in askıya aldığı bir işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d4cf-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="3d4cf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d4cf-121">CommonParameters</span></span>
<span data-ttu-id="3d4cf-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d4cf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d4cf-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d4cf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d4cf-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d4cf-124">INPUTS</span></span>

### <span data-ttu-id="3d4cf-125">System. Guid</span><span class="sxs-lookup"><span data-stu-id="3d4cf-125">System.Guid</span></span>

### <span data-ttu-id="3d4cf-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3d4cf-126">System.String</span></span>

## <span data-ttu-id="3d4cf-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d4cf-127">OUTPUTS</span></span>

### <span data-ttu-id="3d4cf-128">System. void</span><span class="sxs-lookup"><span data-stu-id="3d4cf-128">System.Void</span></span>

## <span data-ttu-id="3d4cf-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d4cf-129">NOTES</span></span>

## <span data-ttu-id="3d4cf-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d4cf-130">RELATED LINKS</span></span>

[<span data-ttu-id="3d4cf-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3d4cf-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="3d4cf-132">Get-Azautomationjoi koyma</span><span class="sxs-lookup"><span data-stu-id="3d4cf-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="3d4cf-133">Özgeçmiş-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3d4cf-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="3d4cf-134">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3d4cf-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


