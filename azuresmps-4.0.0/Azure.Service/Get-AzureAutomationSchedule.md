---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 436A6D6E-2280-475C-A1F5-6A6D72DAD9E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4895c9aa12ad56b8e3ddffb88a19439777d5b54a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105655"
---
# <span data-ttu-id="f207c-101">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f207c-101">Get-AzureAutomationSchedule</span></span>

## <span data-ttu-id="f207c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f207c-102">SYNOPSIS</span></span>

<span data-ttu-id="f207c-103">Bir Azure Otomasyonu zamanlama alır.</span><span class="sxs-lookup"><span data-stu-id="f207c-103">Gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="f207c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f207c-104">SYNTAX</span></span>

### <span data-ttu-id="f207c-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f207c-105">ByAll (Default)</span></span>
```
Get-AzureAutomationSchedule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f207c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f207c-106">ByName</span></span>
```
Get-AzureAutomationSchedule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f207c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f207c-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="f207c-108">**Get-Azureautomationzamanlama** cmdlet 'i, bir Microsoft Azure Automation zamanlaması alır.</span><span class="sxs-lookup"><span data-stu-id="f207c-108">The **Get-AzureAutomationSchedule** cmdlet gets a Microsoft Azure Automation schedule.</span></span>

## <span data-ttu-id="f207c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f207c-109">EXAMPLES</span></span>

### <span data-ttu-id="f207c-110">Örnek 1: zamanlama alma</span><span class="sxs-lookup"><span data-stu-id="f207c-110">Example 1: Get a schedule</span></span>
```
PS C:\> Get-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08"
```

<span data-ttu-id="f207c-111">Bu komut, DailySchedule08 adlı zamanlamayı alır.</span><span class="sxs-lookup"><span data-stu-id="f207c-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="f207c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f207c-112">PARAMETERS</span></span>

### <span data-ttu-id="f207c-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f207c-113">-AutomationAccountName</span></span>
<span data-ttu-id="f207c-114">Azure Otomasyonu hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f207c-114">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="f207c-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f207c-115">-Name</span></span>
<span data-ttu-id="f207c-116">Bir zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f207c-116">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f207c-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="f207c-117">-Profile</span></span>
<span data-ttu-id="f207c-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f207c-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f207c-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f207c-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f207c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f207c-120">CommonParameters</span></span>
<span data-ttu-id="f207c-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f207c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f207c-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f207c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f207c-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f207c-123">INPUTS</span></span>

## <span data-ttu-id="f207c-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f207c-124">OUTPUTS</span></span>

### <span data-ttu-id="f207c-125">Microsoft. Azure. Commands. Automation. model. zamanlama</span><span class="sxs-lookup"><span data-stu-id="f207c-125">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="f207c-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f207c-126">NOTES</span></span>

## <span data-ttu-id="f207c-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f207c-127">RELATED LINKS</span></span>

[<span data-ttu-id="f207c-128">Yeni-Azureautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="f207c-128">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="f207c-129">Remove-Azureautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="f207c-129">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="f207c-130">Set-Azureautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="f207c-130">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


