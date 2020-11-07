---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 9559a599a6d0a50078dbec176ad937947facce7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761482"
---
# <span data-ttu-id="a05a1-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a05a1-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="a05a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a05a1-102">SYNOPSIS</span></span>
<span data-ttu-id="a05a1-103">Otomasyon işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="a05a1-103">Stops an Automation job.</span></span>

## <span data-ttu-id="a05a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a05a1-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a05a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a05a1-105">DESCRIPTION</span></span>
<span data-ttu-id="a05a1-106">**Stop-AzAutomationJob** cmdlet 'ı bir Azure Otomasyonu işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="a05a1-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="a05a1-107">Çalışan bir Otomasyon işi belirtin.</span><span class="sxs-lookup"><span data-stu-id="a05a1-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="a05a1-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a05a1-108">EXAMPLES</span></span>

### <span data-ttu-id="a05a1-109">Örnek 1: işi durdurma</span><span class="sxs-lookup"><span data-stu-id="a05a1-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a05a1-110">Bu komut belirtilen KIMLIĞE sahip işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="a05a1-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="a05a1-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a05a1-111">PARAMETERS</span></span>

### <span data-ttu-id="a05a1-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a05a1-112">-AutomationAccountName</span></span>
<span data-ttu-id="a05a1-113">Bu cmdlet 'in işi durdurduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a05a1-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="a05a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a05a1-114">-DefaultProfile</span></span>
<span data-ttu-id="a05a1-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a05a1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a05a1-116">-ID</span><span class="sxs-lookup"><span data-stu-id="a05a1-116">-Id</span></span>
<span data-ttu-id="a05a1-117">Bu cmdlet 'in durduğu iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a05a1-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="a05a1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a05a1-118">-ResourceGroupName</span></span>
<span data-ttu-id="a05a1-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a05a1-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a05a1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a05a1-120">CommonParameters</span></span>
<span data-ttu-id="a05a1-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a05a1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a05a1-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a05a1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a05a1-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a05a1-123">INPUTS</span></span>

### <span data-ttu-id="a05a1-124">System. Guid</span><span class="sxs-lookup"><span data-stu-id="a05a1-124">System.Guid</span></span>

### <span data-ttu-id="a05a1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a05a1-125">System.String</span></span>

## <span data-ttu-id="a05a1-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a05a1-126">OUTPUTS</span></span>

### <span data-ttu-id="a05a1-127">System. void</span><span class="sxs-lookup"><span data-stu-id="a05a1-127">System.Void</span></span>

## <span data-ttu-id="a05a1-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a05a1-128">NOTES</span></span>

## <span data-ttu-id="a05a1-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a05a1-129">RELATED LINKS</span></span>

[<span data-ttu-id="a05a1-130">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a05a1-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="a05a1-131">Get-Azautomationjoi koyma</span><span class="sxs-lookup"><span data-stu-id="a05a1-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="a05a1-132">Özgeçmiş-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a05a1-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="a05a1-133">Askıya alma-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a05a1-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


