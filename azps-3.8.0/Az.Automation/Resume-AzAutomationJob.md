---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/resume-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
ms.openlocfilehash: 731a2df87ce6ad575e9aa3e10eb124e52ec1b60b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104918"
---
# <span data-ttu-id="7ce42-101">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7ce42-101">Resume-AzAutomationJob</span></span>

## <span data-ttu-id="7ce42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ce42-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce42-103">Askıya alınan Otomasyon işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="7ce42-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="7ce42-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ce42-104">SYNTAX</span></span>

```
Resume-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ce42-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ce42-105">DESCRIPTION</span></span>
<span data-ttu-id="7ce42-106">**Özgeçmiş-AzAutomationJob** cmdlet 'i askıya alınmış bir Azure Otomasyonu işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="7ce42-106">The **Resume-AzAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="7ce42-107">Askıya alınan işi belirtin.</span><span class="sxs-lookup"><span data-stu-id="7ce42-107">Specify the suspended job.</span></span>
<span data-ttu-id="7ce42-108">Bir işi askıya almak için Suspend-AzAutomationJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7ce42-108">To suspend a job, use the Suspend-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="7ce42-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ce42-109">EXAMPLES</span></span>

### <span data-ttu-id="7ce42-110">Örnek 1: askıya alınan işi sürdürme</span><span class="sxs-lookup"><span data-stu-id="7ce42-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7ce42-111">Bu komut belirtilen KIMLIĞE sahip işi sürdürür.</span><span class="sxs-lookup"><span data-stu-id="7ce42-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="7ce42-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ce42-112">PARAMETERS</span></span>

### <span data-ttu-id="7ce42-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7ce42-113">-AutomationAccountName</span></span>
<span data-ttu-id="7ce42-114">Bu cmdlet 'in işi sürdürürecek Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ce42-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="7ce42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ce42-115">-DefaultProfile</span></span>
<span data-ttu-id="7ce42-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7ce42-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ce42-117">-ID</span><span class="sxs-lookup"><span data-stu-id="7ce42-117">-Id</span></span>
<span data-ttu-id="7ce42-118">Bu cmdlet 'in devam eden iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ce42-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="7ce42-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ce42-119">-ResourceGroupName</span></span>
<span data-ttu-id="7ce42-120">Bu cmdlet 'in işi geri aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ce42-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="7ce42-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce42-121">CommonParameters</span></span>
<span data-ttu-id="7ce42-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ce42-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce42-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ce42-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce42-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ce42-124">INPUTS</span></span>

### <span data-ttu-id="7ce42-125">System. Guid</span><span class="sxs-lookup"><span data-stu-id="7ce42-125">System.Guid</span></span>

### <span data-ttu-id="7ce42-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7ce42-126">System.String</span></span>

## <span data-ttu-id="7ce42-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ce42-127">OUTPUTS</span></span>

### <span data-ttu-id="7ce42-128">System. void</span><span class="sxs-lookup"><span data-stu-id="7ce42-128">System.Void</span></span>

## <span data-ttu-id="7ce42-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ce42-129">NOTES</span></span>

## <span data-ttu-id="7ce42-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ce42-130">RELATED LINKS</span></span>

[<span data-ttu-id="7ce42-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7ce42-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="7ce42-132">Get-Azautomationjoi koyma</span><span class="sxs-lookup"><span data-stu-id="7ce42-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="7ce42-133">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7ce42-133">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="7ce42-134">Askıya alma-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7ce42-134">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


