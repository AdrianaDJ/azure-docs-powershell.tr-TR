---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B0AE1969-71FD-4B6E-B0C0-1B744814BD5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93dc73193c300f0f10fd9dccaff1c1f3954b8306
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106032"
---
# <span data-ttu-id="3e2a9-101">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3e2a9-101">Start-AzureAutomationRunbook</span></span>

## <span data-ttu-id="3e2a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e2a9-102">SYNOPSIS</span></span>

<span data-ttu-id="3e2a9-103">Runbook işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="3e2a9-103">Starts a runbook job.</span></span>

## <span data-ttu-id="3e2a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e2a9-104">SYNTAX</span></span>

```
Start-AzureAutomationRunbook -Name <String> [-Parameters <IDictionary>] [-RunOn <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3e2a9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e2a9-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="3e2a9-106">**Start-AzureAutomationRunbook** cmdlet 'ı bir Microsoft Azure Otomasyonu runbook işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="3e2a9-106">The **Start-AzureAutomationRunbook** cmdlet starts a Microsoft Azure Automation runbook job.</span></span>
<span data-ttu-id="3e2a9-107">Runbook 'un KIMLIĞINI veya adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3e2a9-107">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="3e2a9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e2a9-108">EXAMPLES</span></span>

### <span data-ttu-id="3e2a9-109">Örnek 1: runbook işi başlatma</span><span class="sxs-lookup"><span data-stu-id="3e2a9-109">Example 1: Start a runbook job</span></span>
```
PS C:\> Start-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="3e2a9-110">Bu komut, Contoso17 adındaki Otomasyon hesabındaki Runbk01 adındaki runbook için bir runbook işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="3e2a9-110">This command starts a runbook job for the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3e2a9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e2a9-111">PARAMETERS</span></span>

### <span data-ttu-id="3e2a9-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3e2a9-112">-AutomationAccountName</span></span>
<span data-ttu-id="3e2a9-113">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e2a9-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="3e2a9-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="3e2a9-114">-Name</span></span>
<span data-ttu-id="3e2a9-115">Runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e2a9-115">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="3e2a9-116">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="3e2a9-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e2a9-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="3e2a9-117">-Profile</span></span>
<span data-ttu-id="3e2a9-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e2a9-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3e2a9-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3e2a9-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3e2a9-120">-RunOn</span><span class="sxs-lookup"><span data-stu-id="3e2a9-120">-RunOn</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e2a9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e2a9-121">CommonParameters</span></span>
<span data-ttu-id="3e2a9-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e2a9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e2a9-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e2a9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e2a9-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e2a9-124">INPUTS</span></span>

## <span data-ttu-id="3e2a9-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e2a9-125">OUTPUTS</span></span>

### <span data-ttu-id="3e2a9-126">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="3e2a9-126">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="3e2a9-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e2a9-127">NOTES</span></span>

## <span data-ttu-id="3e2a9-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e2a9-128">RELATED LINKS</span></span>

[<span data-ttu-id="3e2a9-129">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3e2a9-129">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="3e2a9-130">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3e2a9-130">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="3e2a9-131">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3e2a9-131">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="3e2a9-132">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3e2a9-132">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="3e2a9-133">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3e2a9-133">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)


