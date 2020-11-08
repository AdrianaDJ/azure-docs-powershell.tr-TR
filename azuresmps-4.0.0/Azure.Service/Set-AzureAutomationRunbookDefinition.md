---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C583BECF-7FC2-4A1F-9788-5CB19E73956C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9464e811597ba0fe5bfe2d53643c7b788c9be71e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106070"
---
# <span data-ttu-id="001fe-101">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="001fe-101">Set-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="001fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="001fe-102">SYNOPSIS</span></span>

<span data-ttu-id="001fe-103">Runbook 'un taslak tanımını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="001fe-103">Updates the draft definition of a runbook.</span></span>

## <span data-ttu-id="001fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="001fe-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbookDefinition -Name <String> -Path <String> [-Overwrite] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="001fe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="001fe-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="001fe-106">**Set-AzureAutomationRunbookDefinition** cmdlet 'ı, Microsoft Azure Otomasyonu runbook 'un taslak tanımını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="001fe-106">The **Set-AzureAutomationRunbookDefinition** cmdlet updates the draft definition of a Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="001fe-107">Taslak runbook 'a sahip bir runbook içeren Windows PowerShell betiği (. ps1) dosyasını belirtin.</span><span class="sxs-lookup"><span data-stu-id="001fe-107">Specify a Windows PowerShell script (.ps1) file that contains a runbook that becomes the draft runbook.</span></span>

<span data-ttu-id="001fe-108">Zaten bir taslak tanımı varsa, var olan taslağın üzerine yazmasını zorlamak için *overwrite* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="001fe-108">If a draft definition already exists, use the *Overwrite* parameter to force the cmdlet to overwrite the existing draft.</span></span>

## <span data-ttu-id="001fe-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="001fe-109">EXAMPLES</span></span>

### <span data-ttu-id="001fe-110">Örnek 1: runbook 'un var olan taslak tanımının üzerine yazma</span><span class="sxs-lookup"><span data-stu-id="001fe-110">Example 1: Overwrite an existing draft definition of a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "Runbk01" -Path ".\App01.ps1" -Overwrite
```

<span data-ttu-id="001fe-111">Bu komut, runbook 'un varolan taslak tanımının üzerine yazar.</span><span class="sxs-lookup"><span data-stu-id="001fe-111">This command overwrites the existing draft definition of a runbook.</span></span>

## <span data-ttu-id="001fe-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="001fe-112">PARAMETERS</span></span>

### <span data-ttu-id="001fe-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="001fe-113">-AutomationAccountName</span></span>
<span data-ttu-id="001fe-114">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="001fe-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="001fe-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="001fe-115">-Name</span></span>
<span data-ttu-id="001fe-116">Bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="001fe-116">Specifies a name.</span></span>

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

### <span data-ttu-id="001fe-117">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="001fe-117">-Overwrite</span></span>
<span data-ttu-id="001fe-118">Var olan bir taslak tanımının üzerine yazılıp yazılmayacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="001fe-118">Indicates whether to overwrite an existing draft definition.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="001fe-119">-Yol</span><span class="sxs-lookup"><span data-stu-id="001fe-119">-Path</span></span>
<span data-ttu-id="001fe-120">Runbook 'un yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="001fe-120">Specifies the path to a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="001fe-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="001fe-121">-Profile</span></span>
<span data-ttu-id="001fe-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="001fe-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="001fe-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="001fe-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="001fe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="001fe-124">CommonParameters</span></span>
<span data-ttu-id="001fe-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="001fe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="001fe-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="001fe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="001fe-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="001fe-127">INPUTS</span></span>

## <span data-ttu-id="001fe-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="001fe-128">OUTPUTS</span></span>

### <span data-ttu-id="001fe-129">Microsoft. Azure. Commands. Automation. model. RunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="001fe-129">Microsoft.Azure.Commands.Automation.Model.RunbookDefinition</span></span>

## <span data-ttu-id="001fe-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="001fe-130">NOTES</span></span>

## <span data-ttu-id="001fe-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="001fe-131">RELATED LINKS</span></span>

[<span data-ttu-id="001fe-132">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="001fe-132">Get-AzureAutomationRunbookDefinition</span></span>](./Get-AzureAutomationRunbookDefinition.md)


