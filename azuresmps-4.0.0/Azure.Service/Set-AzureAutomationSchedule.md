---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E1141271-BA00-455C-AE80-DF5CD00348E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: c0dff4cb86ca46826a1fc7355a9f2c241d8de405
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106071"
---
# <span data-ttu-id="17417-101">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="17417-101">Set-AzureAutomationSchedule</span></span>

## <span data-ttu-id="17417-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17417-102">SYNOPSIS</span></span>

<span data-ttu-id="17417-103">Otomasyon zamanlamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="17417-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="17417-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17417-104">SYNTAX</span></span>

```
Set-AzureAutomationSchedule -Name <String> [-IsEnabled <Boolean>] [-Description <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="17417-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="17417-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="17417-106">**Set-Azureautomationzamanlama** cmdlet 'ı, Microsoft Azure Otomasyonu 'nda bir zamanlamayı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="17417-106">The **Set-AzureAutomationSchedule** cmdlet modifies a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="17417-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17417-107">EXAMPLES</span></span>

### <span data-ttu-id="17417-108">Örnek 1: zamanlamayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="17417-108">Example 1: Modify a schedule</span></span>
```
PS C:\> Set-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule"
```

<span data-ttu-id="17417-109">Bu komut, Schedule01 adlı zamanlamanın açıklamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="17417-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="17417-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17417-110">PARAMETERS</span></span>

### <span data-ttu-id="17417-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="17417-111">-AutomationAccountName</span></span>
<span data-ttu-id="17417-112">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17417-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="17417-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="17417-113">-Description</span></span>
<span data-ttu-id="17417-114">Zamanlama için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="17417-114">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17417-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="17417-115">-IsEnabled</span></span>
<span data-ttu-id="17417-116">Zamanlamanın etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="17417-116">Indicates whether the schedule is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17417-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="17417-117">-Name</span></span>
<span data-ttu-id="17417-118">Zamanlama için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="17417-118">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="17417-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="17417-119">-Profile</span></span>
<span data-ttu-id="17417-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17417-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="17417-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="17417-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="17417-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17417-122">CommonParameters</span></span>
<span data-ttu-id="17417-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17417-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17417-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17417-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17417-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17417-125">INPUTS</span></span>

## <span data-ttu-id="17417-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17417-126">OUTPUTS</span></span>

### <span data-ttu-id="17417-127">Microsoft. Azure. Commands. Automation. model. zamanlama</span><span class="sxs-lookup"><span data-stu-id="17417-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="17417-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17417-128">NOTES</span></span>

## <span data-ttu-id="17417-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17417-129">RELATED LINKS</span></span>

[<span data-ttu-id="17417-130">Get-Azureautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="17417-130">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="17417-131">Yeni-Azureautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="17417-131">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="17417-132">Remove-Azureautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="17417-132">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)


