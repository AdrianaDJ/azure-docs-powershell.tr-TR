---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2E363D6B-7A05-4C54-B005-68FDBA49A105
online version: ''
schema: 2.0.0
ms.openlocfilehash: cda64b916635d3b46ffb7e8b4170330810a95b5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105942"
---
# <span data-ttu-id="ebedf-101">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ebedf-101">Stop-AzureAutomationJob</span></span>

## <span data-ttu-id="ebedf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebedf-102">SYNOPSIS</span></span>

<span data-ttu-id="ebedf-103">Otomasyon işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="ebedf-103">Stops an Automation job.</span></span>

## <span data-ttu-id="ebedf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ebedf-104">SYNTAX</span></span>

```
Stop-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebedf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ebedf-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ebedf-106">**Stop-AzureAutomationJob** cmdlet 'ı bir Microsoft Azure Otomasyonu işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="ebedf-106">The **Stop-AzureAutomationJob** cmdlet stops a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="ebedf-107">Çalışan bir Otomasyon işi belirtin.</span><span class="sxs-lookup"><span data-stu-id="ebedf-107">Specify a running automation job.</span></span>

## <span data-ttu-id="ebedf-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ebedf-108">EXAMPLES</span></span>

### <span data-ttu-id="ebedf-109">Örnek 1: işi durdurma</span><span class="sxs-lookup"><span data-stu-id="ebedf-109">Example 1: Stop a job</span></span>
```
PS C:\> Stop-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="ebedf-110">Bu komut belirtilen KIMLIĞE sahip işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="ebedf-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="ebedf-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ebedf-111">PARAMETERS</span></span>

### <span data-ttu-id="ebedf-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ebedf-112">-AutomationAccountName</span></span>
<span data-ttu-id="ebedf-113">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebedf-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="ebedf-114">-ID</span><span class="sxs-lookup"><span data-stu-id="ebedf-114">-Id</span></span>
<span data-ttu-id="ebedf-115">İşin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebedf-115">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="ebedf-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="ebedf-116">-Profile</span></span>
<span data-ttu-id="ebedf-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebedf-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ebedf-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ebedf-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ebedf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebedf-119">CommonParameters</span></span>
<span data-ttu-id="ebedf-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ebedf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebedf-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebedf-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebedf-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ebedf-122">INPUTS</span></span>

## <span data-ttu-id="ebedf-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ebedf-123">OUTPUTS</span></span>

## <span data-ttu-id="ebedf-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ebedf-124">NOTES</span></span>

## <span data-ttu-id="ebedf-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ebedf-125">RELATED LINKS</span></span>

[<span data-ttu-id="ebedf-126">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ebedf-126">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="ebedf-127">Özgeçmiş-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ebedf-127">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="ebedf-128">Askıya alma-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ebedf-128">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


