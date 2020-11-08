---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 304F71E0-9E89-46E6-BD25-7584601CC845
online version: ''
schema: 2.0.0
ms.openlocfilehash: e507b1b35bf8739c80bbdf92f02f29099ceb3284
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105657"
---
# <span data-ttu-id="88c26-101">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="88c26-101">Get-AzureAutomationRunbook</span></span>

## <span data-ttu-id="88c26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88c26-102">SYNOPSIS</span></span>

<span data-ttu-id="88c26-103">Runbook alır.</span><span class="sxs-lookup"><span data-stu-id="88c26-103">Gets a runbook.</span></span>

## <span data-ttu-id="88c26-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88c26-104">SYNTAX</span></span>

### <span data-ttu-id="88c26-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="88c26-105">ByAll (Default)</span></span>
```
Get-AzureAutomationRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="88c26-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="88c26-106">ByRunbookName</span></span>
```
Get-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="88c26-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="88c26-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="88c26-108">**Get-AzureAutomationRunbook** cmdlet 'i bir veya daha fazla Microsoft Azure Automation runbook 'unu alır.</span><span class="sxs-lookup"><span data-stu-id="88c26-108">The **Get-AzureAutomationRunbook** cmdlet gets one or more Microsoft Azure Automation runbooks.</span></span>
<span data-ttu-id="88c26-109">Varsayılan olarak, tüm runbook 'lar döndürülür.</span><span class="sxs-lookup"><span data-stu-id="88c26-109">By default, all runbooks are returned.</span></span>
<span data-ttu-id="88c26-110">Belirli bir runbook almak için adını veya KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="88c26-110">To get a specific runbook, specify its name or ID.</span></span>
<span data-ttu-id="88c26-111">Belirli bir zamanlamaya bağlı tüm runbook 'ları almak için, zamanlama adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="88c26-111">To get all runbooks linked to a specific schedule, specify the schedule name.</span></span>

## <span data-ttu-id="88c26-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88c26-112">EXAMPLES</span></span>

### <span data-ttu-id="88c26-113">Örnek 1: tüm runbook 'ları alma</span><span class="sxs-lookup"><span data-stu-id="88c26-113">Example 1: Get all runbooks</span></span>
```
PS C:\> Get-AzureAutomationRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="88c26-114">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki tüm runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="88c26-114">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="88c26-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88c26-115">PARAMETERS</span></span>

### <span data-ttu-id="88c26-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="88c26-116">-AutomationAccountName</span></span>
<span data-ttu-id="88c26-117">Azure Otomasyonu hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="88c26-117">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="88c26-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="88c26-118">-Name</span></span>
<span data-ttu-id="88c26-119">Runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="88c26-119">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88c26-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="88c26-120">-Profile</span></span>
<span data-ttu-id="88c26-121">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="88c26-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="88c26-122">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="88c26-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="88c26-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88c26-123">CommonParameters</span></span>
<span data-ttu-id="88c26-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88c26-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88c26-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88c26-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88c26-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88c26-126">INPUTS</span></span>

## <span data-ttu-id="88c26-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88c26-127">OUTPUTS</span></span>

### <span data-ttu-id="88c26-128">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="88c26-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="88c26-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88c26-129">NOTES</span></span>

## <span data-ttu-id="88c26-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88c26-130">RELATED LINKS</span></span>

[<span data-ttu-id="88c26-131">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="88c26-131">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="88c26-132">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="88c26-132">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="88c26-133">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="88c26-133">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="88c26-134">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="88c26-134">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="88c26-135">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="88c26-135">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


