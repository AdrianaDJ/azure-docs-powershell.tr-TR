---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
ms.openlocfilehash: 6d23fe3728b569cbb1a2aee498d560672ee75877
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591165"
---
# <span data-ttu-id="64d00-101">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="64d00-101">Resume-AzureRmAutomationJob</span></span>

## <span data-ttu-id="64d00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64d00-102">SYNOPSIS</span></span>
<span data-ttu-id="64d00-103">Askıya alınan Otomasyon işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="64d00-103">Resumes a suspended Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64d00-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64d00-104">SYNTAX</span></span>

```
Resume-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64d00-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="64d00-105">DESCRIPTION</span></span>
<span data-ttu-id="64d00-106">**Özgeçmiş-AzureRmAutomationJob** cmdlet 'i askıya alınmış bir Azure Otomasyonu işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="64d00-106">The **Resume-AzureRmAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="64d00-107">Askıya alınan işi belirtin.</span><span class="sxs-lookup"><span data-stu-id="64d00-107">Specify the suspended job.</span></span>

<span data-ttu-id="64d00-108">Bir işi askıya almak için Suspend-AzureRmAutomationJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="64d00-108">To suspend a job, use the Suspend-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="64d00-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64d00-109">EXAMPLES</span></span>

### <span data-ttu-id="64d00-110">Örnek 1: askıya alınan işi sürdürme</span><span class="sxs-lookup"><span data-stu-id="64d00-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="64d00-111">Bu komut belirtilen KIMLIĞE sahip işi sürdürür.</span><span class="sxs-lookup"><span data-stu-id="64d00-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="64d00-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64d00-112">PARAMETERS</span></span>

### <span data-ttu-id="64d00-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="64d00-113">-AutomationAccountName</span></span>
<span data-ttu-id="64d00-114">Bu cmdlet 'in işi sürdürürecek Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64d00-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="64d00-115">-ID</span><span class="sxs-lookup"><span data-stu-id="64d00-115">-Id</span></span>
<span data-ttu-id="64d00-116">Bu cmdlet 'in devam eden iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="64d00-116">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="64d00-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64d00-117">-ResourceGroupName</span></span>
<span data-ttu-id="64d00-118">Bu cmdlet 'in işi geri aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64d00-118">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="64d00-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d00-119">-DefaultProfile</span></span>
<span data-ttu-id="64d00-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="64d00-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64d00-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d00-121">CommonParameters</span></span>
<span data-ttu-id="64d00-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64d00-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d00-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64d00-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d00-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64d00-124">INPUTS</span></span>

## <span data-ttu-id="64d00-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64d00-125">OUTPUTS</span></span>

## <span data-ttu-id="64d00-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64d00-126">NOTES</span></span>

## <span data-ttu-id="64d00-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64d00-127">RELATED LINKS</span></span>

[<span data-ttu-id="64d00-128">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="64d00-128">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="64d00-129">Get-Azurermautomationjoi yerleştir</span><span class="sxs-lookup"><span data-stu-id="64d00-129">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="64d00-130">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="64d00-130">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="64d00-131">Askıya al-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="64d00-131">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


