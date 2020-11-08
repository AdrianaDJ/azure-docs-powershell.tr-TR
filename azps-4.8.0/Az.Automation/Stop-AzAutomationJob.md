---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 451457cf4483d9af6d8a7aca8731b95dc5c95859
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108502"
---
# <span data-ttu-id="d61af-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d61af-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="d61af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d61af-102">SYNOPSIS</span></span>
<span data-ttu-id="d61af-103">Otomasyon işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="d61af-103">Stops an Automation job.</span></span>

## <span data-ttu-id="d61af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d61af-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d61af-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d61af-105">DESCRIPTION</span></span>
<span data-ttu-id="d61af-106">**Stop-AzAutomationJob** cmdlet 'ı bir Azure Otomasyonu işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="d61af-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="d61af-107">Çalışan bir Otomasyon işi belirtin.</span><span class="sxs-lookup"><span data-stu-id="d61af-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="d61af-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d61af-108">EXAMPLES</span></span>

### <span data-ttu-id="d61af-109">Örnek 1: işi durdurma</span><span class="sxs-lookup"><span data-stu-id="d61af-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d61af-110">Bu komut belirtilen KIMLIĞE sahip işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="d61af-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="d61af-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d61af-111">PARAMETERS</span></span>

### <span data-ttu-id="d61af-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d61af-112">-AutomationAccountName</span></span>
<span data-ttu-id="d61af-113">Bu cmdlet 'in işi durdurduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d61af-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="d61af-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d61af-114">-DefaultProfile</span></span>
<span data-ttu-id="d61af-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d61af-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d61af-116">-ID</span><span class="sxs-lookup"><span data-stu-id="d61af-116">-Id</span></span>
<span data-ttu-id="d61af-117">Bu cmdlet 'in durduğu iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d61af-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d61af-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d61af-118">-ResourceGroupName</span></span>
<span data-ttu-id="d61af-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d61af-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d61af-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d61af-120">CommonParameters</span></span>
<span data-ttu-id="d61af-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d61af-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d61af-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d61af-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d61af-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d61af-123">INPUTS</span></span>

### <span data-ttu-id="d61af-124">System. Guid</span><span class="sxs-lookup"><span data-stu-id="d61af-124">System.Guid</span></span>

### <span data-ttu-id="d61af-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d61af-125">System.String</span></span>

## <span data-ttu-id="d61af-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d61af-126">OUTPUTS</span></span>

### <span data-ttu-id="d61af-127">System. void</span><span class="sxs-lookup"><span data-stu-id="d61af-127">System.Void</span></span>

## <span data-ttu-id="d61af-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d61af-128">NOTES</span></span>

## <span data-ttu-id="d61af-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d61af-129">RELATED LINKS</span></span>

[<span data-ttu-id="d61af-130">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d61af-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="d61af-131">Get-Azautomationjoi koyma</span><span class="sxs-lookup"><span data-stu-id="d61af-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="d61af-132">Özgeçmiş-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d61af-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="d61af-133">Askıya alma-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d61af-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


