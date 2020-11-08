---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CE04DEE6-28AE-43A3-A8DE-98AC0A57E575
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1c2d9a3aa53cb8efd2924f24aa80db2c7fd07fea
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105759"
---
# <span data-ttu-id="8ced9-101">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8ced9-101">Suspend-AzureAutomationJob</span></span>

## <span data-ttu-id="8ced9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ced9-102">SYNOPSIS</span></span>

<span data-ttu-id="8ced9-103">Otomasyon işini askıya alır.</span><span class="sxs-lookup"><span data-stu-id="8ced9-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="8ced9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ced9-104">SYNTAX</span></span>

```
Suspend-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ced9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ced9-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="8ced9-106">**Askıya al-AzureAutomationJob** cmdlet 'ı bir Microsoft Azure Otomasyonu işini askıya alır.</span><span class="sxs-lookup"><span data-stu-id="8ced9-106">The **Suspend-AzureAutomationJob** cmdlet suspends a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="8ced9-107">Çalışan bir Otomasyon işi belirtin.</span><span class="sxs-lookup"><span data-stu-id="8ced9-107">Specify a running Automation job.</span></span>

<span data-ttu-id="8ced9-108">Askıya alınmış bir işi sürdürmek için **Resume-AzureAutomationJob** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8ced9-108">To resume a suspended job, use the **Resume-AzureAutomationJob** cmdlet.</span></span>

## <span data-ttu-id="8ced9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ced9-109">EXAMPLES</span></span>

### <span data-ttu-id="8ced9-110">Örnek 1: işi askıya alma</span><span class="sxs-lookup"><span data-stu-id="8ced9-110">Example 1: Suspend a job</span></span>
```
PS C:\> Suspend-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="8ced9-111">Bu komut belirtilen KIMLIĞE sahip işi askıya alır.</span><span class="sxs-lookup"><span data-stu-id="8ced9-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="8ced9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ced9-112">PARAMETERS</span></span>

### <span data-ttu-id="8ced9-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8ced9-113">-AutomationAccountName</span></span>
<span data-ttu-id="8ced9-114">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ced9-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="8ced9-115">-ID</span><span class="sxs-lookup"><span data-stu-id="8ced9-115">-Id</span></span>
<span data-ttu-id="8ced9-116">İşin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ced9-116">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="8ced9-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="8ced9-117">-Profile</span></span>
<span data-ttu-id="8ced9-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ced9-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8ced9-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="8ced9-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8ced9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ced9-120">CommonParameters</span></span>
<span data-ttu-id="8ced9-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ced9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ced9-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ced9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ced9-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ced9-123">INPUTS</span></span>

## <span data-ttu-id="8ced9-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ced9-124">OUTPUTS</span></span>

## <span data-ttu-id="8ced9-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ced9-125">NOTES</span></span>

## <span data-ttu-id="8ced9-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ced9-126">RELATED LINKS</span></span>

[<span data-ttu-id="8ced9-127">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8ced9-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="8ced9-128">Özgeçmiş-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8ced9-128">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="8ced9-129">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8ced9-129">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)


