---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
ms.openlocfilehash: 67100c80a3a0ca822fc1f37f63968be282925b76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587306"
---
# <span data-ttu-id="3cc2f-101">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3cc2f-101">Stop-AzureRmAutomationJob</span></span>

## <span data-ttu-id="3cc2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cc2f-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc2f-103">Otomasyon işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="3cc2f-103">Stops an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cc2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3cc2f-104">SYNTAX</span></span>

```
Stop-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cc2f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3cc2f-105">DESCRIPTION</span></span>
<span data-ttu-id="3cc2f-106">**Stop-AzureRmAutomationJob** cmdlet 'ı bir Azure Otomasyonu işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="3cc2f-106">The **Stop-AzureRmAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="3cc2f-107">Çalışan bir Otomasyon işi belirtin.</span><span class="sxs-lookup"><span data-stu-id="3cc2f-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="3cc2f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3cc2f-108">EXAMPLES</span></span>

### <span data-ttu-id="3cc2f-109">Örnek 1: işi durdurma</span><span class="sxs-lookup"><span data-stu-id="3cc2f-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3cc2f-110">Bu komut belirtilen KIMLIĞE sahip işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="3cc2f-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="3cc2f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3cc2f-111">PARAMETERS</span></span>

### <span data-ttu-id="3cc2f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3cc2f-112">-AutomationAccountName</span></span>
<span data-ttu-id="3cc2f-113">Bu cmdlet 'in işi durdurduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3cc2f-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="3cc2f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc2f-114">-DefaultProfile</span></span>
<span data-ttu-id="3cc2f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3cc2f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cc2f-116">-ID</span><span class="sxs-lookup"><span data-stu-id="3cc2f-116">-Id</span></span>
<span data-ttu-id="3cc2f-117">Bu cmdlet 'in durduğu iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3cc2f-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="3cc2f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cc2f-118">-ResourceGroupName</span></span>
<span data-ttu-id="3cc2f-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3cc2f-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3cc2f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc2f-120">CommonParameters</span></span>
<span data-ttu-id="3cc2f-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3cc2f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc2f-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cc2f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc2f-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3cc2f-123">INPUTS</span></span>

### <span data-ttu-id="3cc2f-124">System. Guid</span><span class="sxs-lookup"><span data-stu-id="3cc2f-124">System.Guid</span></span>

### <span data-ttu-id="3cc2f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3cc2f-125">System.String</span></span>

## <span data-ttu-id="3cc2f-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3cc2f-126">OUTPUTS</span></span>

### <span data-ttu-id="3cc2f-127">System. void</span><span class="sxs-lookup"><span data-stu-id="3cc2f-127">System.Void</span></span>

## <span data-ttu-id="3cc2f-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3cc2f-128">NOTES</span></span>

## <span data-ttu-id="3cc2f-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3cc2f-129">RELATED LINKS</span></span>

[<span data-ttu-id="3cc2f-130">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3cc2f-130">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="3cc2f-131">Get-Azurermautomationjoi yerleştir</span><span class="sxs-lookup"><span data-stu-id="3cc2f-131">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="3cc2f-132">Özgeçmiş-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3cc2f-132">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="3cc2f-133">Askıya al-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3cc2f-133">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


