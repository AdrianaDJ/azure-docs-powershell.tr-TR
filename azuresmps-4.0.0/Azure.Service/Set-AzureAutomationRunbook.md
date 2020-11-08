---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C24CFC83-3151-452D-A7B9-E78466493474
online version: ''
schema: 2.0.0
ms.openlocfilehash: e193dba6f64553e5e52d7f900bdc5c54deac5112
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106072"
---
# <span data-ttu-id="a95c9-101">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a95c9-101">Set-AzureAutomationRunbook</span></span>

## <span data-ttu-id="a95c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a95c9-102">SYNOPSIS</span></span>

<span data-ttu-id="a95c9-103">Runbook yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a95c9-103">Modifies the configuration of a runbook.</span></span>

## <span data-ttu-id="a95c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a95c9-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a95c9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a95c9-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="a95c9-106">**Set-AzureAutomationRunbook** cmdlet 'ı, Microsoft Azure Otomasyonu runbook 'un yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a95c9-106">The **Set-AzureAutomationRunbook** cmdlet modifies the configuration of a Microsoft Azure Automation runbook.</span></span>

## <span data-ttu-id="a95c9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a95c9-107">EXAMPLES</span></span>

### <span data-ttu-id="a95c9-108">Örnek 1: runbook için ayrıntılı günlüğü etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a95c9-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook" -LogVerbose $True
```

<span data-ttu-id="a95c9-109">Bu komut, Contoso17 adlı Otomasyon hesabında belirtilen runbook işlerinin ayrıntılı kaydını etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="a95c9-109">This command enables verbose logging for the jobs of the specified runbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a95c9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a95c9-110">PARAMETERS</span></span>

### <span data-ttu-id="a95c9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a95c9-111">-AutomationAccountName</span></span>
<span data-ttu-id="a95c9-112">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a95c9-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="a95c9-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="a95c9-113">-Description</span></span>
<span data-ttu-id="a95c9-114">Runbook için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="a95c9-114">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="a95c9-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="a95c9-115">-LogProgress</span></span>
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

### <span data-ttu-id="a95c9-116">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="a95c9-116">-LogVerbose</span></span>
<span data-ttu-id="a95c9-117">Ayrıntılı günlüğün kullanılıp kullanılmayacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a95c9-117">Indicates whether to use verbose logging.</span></span>

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

### <span data-ttu-id="a95c9-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a95c9-118">-Name</span></span>
<span data-ttu-id="a95c9-119">Bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="a95c9-119">Specifies a name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95c9-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="a95c9-120">-Profile</span></span>
<span data-ttu-id="a95c9-121">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a95c9-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a95c9-122">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a95c9-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a95c9-123">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="a95c9-123">-Tags</span></span>
<span data-ttu-id="a95c9-124">Etiket dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a95c9-124">Specifies an array of tags.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95c9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95c9-125">CommonParameters</span></span>
<span data-ttu-id="a95c9-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a95c9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95c9-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a95c9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95c9-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a95c9-128">INPUTS</span></span>

## <span data-ttu-id="a95c9-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a95c9-129">OUTPUTS</span></span>

### <span data-ttu-id="a95c9-130">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="a95c9-130">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="a95c9-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a95c9-131">NOTES</span></span>

## <span data-ttu-id="a95c9-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a95c9-132">RELATED LINKS</span></span>

[<span data-ttu-id="a95c9-133">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a95c9-133">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="a95c9-134">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a95c9-134">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="a95c9-135">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a95c9-135">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="a95c9-136">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a95c9-136">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="a95c9-137">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a95c9-137">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


