---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 5E5B8102-9E7E-4128-8160-3AA3803B118F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ff0831e6458a9d587b508acfa2e09948d81d87e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105462"
---
# <span data-ttu-id="e412e-101">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e412e-101">Resume-AzureAutomationJob</span></span>

## <span data-ttu-id="e412e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e412e-102">SYNOPSIS</span></span>

<span data-ttu-id="e412e-103">Askıya alınan Otomasyon işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="e412e-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="e412e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e412e-104">SYNTAX</span></span>

```
Resume-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e412e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e412e-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e412e-106">**Özgeçmiş-AzureAutomationJob** cmdlet 'i askıya alınan bir Microsoft Azure Otomasyonu işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="e412e-106">The **Resume-AzureAutomationJob** cmdlet resumes a suspended Microsoft Azure Automation job.</span></span>
<span data-ttu-id="e412e-107">Askıya alınan işi belirtmek için *ID* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e412e-107">Use the *Id* parameter to specify the suspended job.</span></span>

<span data-ttu-id="e412e-108">Bir işi askıya almak için Suspend-AzureAutomationJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e412e-108">To suspend a job, use the Suspend-AzureAutomationJob cmdlet.</span></span>

## <span data-ttu-id="e412e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e412e-109">EXAMPLES</span></span>

### <span data-ttu-id="e412e-110">Örnek 1: askıya alınan işi sürdürme</span><span class="sxs-lookup"><span data-stu-id="e412e-110">Example 1: Resume a suspended job</span></span>
```
PS C:\> Resume-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="e412e-111">Bu komut belirtilen KIMLIĞE sahip işi sürdürür.</span><span class="sxs-lookup"><span data-stu-id="e412e-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="e412e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e412e-112">PARAMETERS</span></span>

### <span data-ttu-id="e412e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e412e-113">-AutomationAccountName</span></span>
<span data-ttu-id="e412e-114">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e412e-114">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e412e-115">-ID</span><span class="sxs-lookup"><span data-stu-id="e412e-115">-Id</span></span>
<span data-ttu-id="e412e-116">İşin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e412e-116">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e412e-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="e412e-117">-Profile</span></span>
<span data-ttu-id="e412e-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e412e-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e412e-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e412e-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e412e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e412e-120">CommonParameters</span></span>
<span data-ttu-id="e412e-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e412e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e412e-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e412e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e412e-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e412e-123">INPUTS</span></span>

## <span data-ttu-id="e412e-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e412e-124">OUTPUTS</span></span>

## <span data-ttu-id="e412e-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e412e-125">NOTES</span></span>

## <span data-ttu-id="e412e-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e412e-126">RELATED LINKS</span></span>

[<span data-ttu-id="e412e-127">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e412e-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="e412e-128">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e412e-128">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="e412e-129">Askıya alma-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e412e-129">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


