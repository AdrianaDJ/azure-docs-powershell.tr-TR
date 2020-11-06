---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
ms.openlocfilehash: db7e76a21f635429be598ca9f40899ece3fa0406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593837"
---
# <span data-ttu-id="d6e10-101">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d6e10-101">Stop-AzureRmAutomationJob</span></span>

## <span data-ttu-id="d6e10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6e10-102">SYNOPSIS</span></span>
<span data-ttu-id="d6e10-103">Otomasyon işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="d6e10-103">Stops an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6e10-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6e10-104">SYNTAX</span></span>

```
Stop-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6e10-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6e10-105">DESCRIPTION</span></span>
<span data-ttu-id="d6e10-106">**Stop-AzureRmAutomationJob** cmdlet 'ı bir Azure Otomasyonu işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="d6e10-106">The **Stop-AzureRmAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="d6e10-107">Çalışan bir Otomasyon işi belirtin.</span><span class="sxs-lookup"><span data-stu-id="d6e10-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="d6e10-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6e10-108">EXAMPLES</span></span>

### <span data-ttu-id="d6e10-109">Örnek 1: işi durdurma</span><span class="sxs-lookup"><span data-stu-id="d6e10-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d6e10-110">Bu komut belirtilen KIMLIĞE sahip işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="d6e10-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="d6e10-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6e10-111">PARAMETERS</span></span>

### <span data-ttu-id="d6e10-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d6e10-112">-AutomationAccountName</span></span>
<span data-ttu-id="d6e10-113">Bu cmdlet 'in işi durdurduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6e10-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="d6e10-114">-ID</span><span class="sxs-lookup"><span data-stu-id="d6e10-114">-Id</span></span>
<span data-ttu-id="d6e10-115">Bu cmdlet 'in durduğu iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6e10-115">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d6e10-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6e10-116">-ResourceGroupName</span></span>
<span data-ttu-id="d6e10-117">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6e10-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d6e10-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6e10-118">-DefaultProfile</span></span>
<span data-ttu-id="d6e10-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d6e10-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6e10-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6e10-120">CommonParameters</span></span>
<span data-ttu-id="d6e10-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6e10-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6e10-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6e10-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6e10-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6e10-123">INPUTS</span></span>

## <span data-ttu-id="d6e10-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6e10-124">OUTPUTS</span></span>

## <span data-ttu-id="d6e10-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6e10-125">NOTES</span></span>

## <span data-ttu-id="d6e10-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6e10-126">RELATED LINKS</span></span>

[<span data-ttu-id="d6e10-127">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d6e10-127">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="d6e10-128">Get-Azurermautomationjoi yerleştir</span><span class="sxs-lookup"><span data-stu-id="d6e10-128">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="d6e10-129">Özgeçmiş-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d6e10-129">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="d6e10-130">Askıya al-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d6e10-130">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


