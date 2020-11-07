---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/suspend-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
ms.openlocfilehash: 05747721219610524e0a245df5b5a67e8e69b483
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592969"
---
# <span data-ttu-id="912b2-101">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="912b2-101">Suspend-AzureRmAutomationJob</span></span>

## <span data-ttu-id="912b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="912b2-102">SYNOPSIS</span></span>
<span data-ttu-id="912b2-103">Otomasyon işini askıya alır.</span><span class="sxs-lookup"><span data-stu-id="912b2-103">Suspends an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="912b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="912b2-104">SYNTAX</span></span>

```
Suspend-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="912b2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="912b2-105">DESCRIPTION</span></span>
<span data-ttu-id="912b2-106">**Askıya alma-AzureRmAutomationJob** cmdlet 'ı bir Azure Otomasyonu işini askıya alır.</span><span class="sxs-lookup"><span data-stu-id="912b2-106">The **Suspend-AzureRmAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="912b2-107">Çalışan bir Otomasyon işi belirtin.</span><span class="sxs-lookup"><span data-stu-id="912b2-107">Specify a running Automation job.</span></span>

<span data-ttu-id="912b2-108">Askıya alınmış bir işi sürdürmek için Resume-AzureRmAutomationJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="912b2-108">To resume a suspended job, use the Resume-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="912b2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="912b2-109">EXAMPLES</span></span>

### <span data-ttu-id="912b2-110">Örnek 1: işi askıya alma</span><span class="sxs-lookup"><span data-stu-id="912b2-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="912b2-111">Bu komut belirtilen KIMLIĞE sahip işi askıya alır.</span><span class="sxs-lookup"><span data-stu-id="912b2-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="912b2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="912b2-112">PARAMETERS</span></span>

### <span data-ttu-id="912b2-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="912b2-113">-AutomationAccountName</span></span>
<span data-ttu-id="912b2-114">Bu cmdlet 'in işi askıya aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="912b2-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="912b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="912b2-115">-DefaultProfile</span></span>
<span data-ttu-id="912b2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="912b2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="912b2-117">-ID</span><span class="sxs-lookup"><span data-stu-id="912b2-117">-Id</span></span>
<span data-ttu-id="912b2-118">Bu cmdlet 'in askıya aldığı bir işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="912b2-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912b2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="912b2-119">-ResourceGroupName</span></span>
<span data-ttu-id="912b2-120">Bu cmdlet 'in askıya aldığı bir işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="912b2-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="912b2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="912b2-121">CommonParameters</span></span>
<span data-ttu-id="912b2-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="912b2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="912b2-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="912b2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="912b2-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="912b2-124">INPUTS</span></span>

### <span data-ttu-id="912b2-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="912b2-125">None</span></span>
<span data-ttu-id="912b2-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="912b2-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="912b2-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="912b2-127">OUTPUTS</span></span>

## <span data-ttu-id="912b2-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="912b2-128">NOTES</span></span>

## <span data-ttu-id="912b2-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="912b2-129">RELATED LINKS</span></span>

[<span data-ttu-id="912b2-130">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="912b2-130">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="912b2-131">Get-Azurermautomationjoi yerleştir</span><span class="sxs-lookup"><span data-stu-id="912b2-131">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="912b2-132">Özgeçmiş-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="912b2-132">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="912b2-133">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="912b2-133">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

