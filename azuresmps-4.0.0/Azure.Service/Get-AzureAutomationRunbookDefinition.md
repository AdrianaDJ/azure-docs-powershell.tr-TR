---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 66740917-E8BB-44ED-9CBB-9825BD1840E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b049d770dbcee8b7cea56dbadbf7d4071c344cc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106362"
---
# <span data-ttu-id="170ef-101">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="170ef-101">Get-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="170ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="170ef-102">SYNOPSIS</span></span>

<span data-ttu-id="170ef-103">Runbook tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="170ef-103">Gets a runbook definition.</span></span>

## <span data-ttu-id="170ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="170ef-104">SYNTAX</span></span>

```
Get-AzureAutomationRunbookDefinition -Name <String> [-Slot <String>] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="170ef-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="170ef-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="170ef-106">**Get-AzureAutomationRunbookDefinition** cmdlet 'i, bir Azure Otomasyonu runbook 'un taslak tanımını, yayınlanan tanımını veya her ikisini de alır.</span><span class="sxs-lookup"><span data-stu-id="170ef-106">The **Get-AzureAutomationRunbookDefinition** cmdlet gets the draft definition, the published definition, or both definitions of an Azure Automation runbook.</span></span>
<span data-ttu-id="170ef-107">Varsayılan olarak, yayımlanan sürüm verilir.</span><span class="sxs-lookup"><span data-stu-id="170ef-107">By default, the published version is returned.</span></span>

## <span data-ttu-id="170ef-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="170ef-108">EXAMPLES</span></span>

### <span data-ttu-id="170ef-109">Örnek 1: runbook tanımını alma</span><span class="sxs-lookup"><span data-stu-id="170ef-109">Example 1: Get a runbook definition</span></span>
```
PS C:\> Get-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "RunbookDef01" -Slot "Published"
```

<span data-ttu-id="170ef-110">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki RunbookDef01 adındaki runbook 'un yayımlanmış runbook tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="170ef-110">This command gets the published runbook definition of the runbook named RunbookDef01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="170ef-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="170ef-111">PARAMETERS</span></span>

### <span data-ttu-id="170ef-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="170ef-112">-AutomationAccountName</span></span>
<span data-ttu-id="170ef-113">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="170ef-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="170ef-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="170ef-114">-Name</span></span>
<span data-ttu-id="170ef-115">Runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="170ef-115">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="170ef-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="170ef-116">-Profile</span></span>
<span data-ttu-id="170ef-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="170ef-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="170ef-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="170ef-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="170ef-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="170ef-119">-Slot</span></span>
<span data-ttu-id="170ef-120">Yuvayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="170ef-120">Specifies the slot.</span></span>
<span data-ttu-id="170ef-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="170ef-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="170ef-122">Lar</span><span class="sxs-lookup"><span data-stu-id="170ef-122">Draft</span></span>
- <span data-ttu-id="170ef-123">Yayımlanabilir</span><span class="sxs-lookup"><span data-stu-id="170ef-123">Published</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="170ef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170ef-124">CommonParameters</span></span>
<span data-ttu-id="170ef-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="170ef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170ef-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="170ef-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170ef-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="170ef-127">INPUTS</span></span>

## <span data-ttu-id="170ef-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="170ef-128">OUTPUTS</span></span>

## <span data-ttu-id="170ef-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="170ef-129">NOTES</span></span>

## <span data-ttu-id="170ef-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="170ef-130">RELATED LINKS</span></span>

[<span data-ttu-id="170ef-131">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="170ef-131">Set-AzureAutomationRunbookDefinition</span></span>](./Set-AzureAutomationRunbookDefinition.md)


