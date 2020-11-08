---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0B496085-670D-45F7-B989-D4541A3811FF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37d95c570cc1c12bc40704ec2a2d89fcbec7cf48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105934"
---
# <span data-ttu-id="8451c-101">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8451c-101">New-AzureAutomationRunbook</span></span>

## <span data-ttu-id="8451c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8451c-102">SYNOPSIS</span></span>

<span data-ttu-id="8451c-103">Runbook oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8451c-103">Creates a runbook.</span></span>

## <span data-ttu-id="8451c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8451c-104">SYNTAX</span></span>

### <span data-ttu-id="8451c-105">ByRunbookName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8451c-105">ByRunbookName (Default)</span></span>
```
New-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8451c-106">ByPath</span><span class="sxs-lookup"><span data-stu-id="8451c-106">ByPath</span></span>
```
New-AzureAutomationRunbook -Path <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8451c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8451c-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="8451c-108">**New-AzureAutomationRunbook** cmdlet 'i yeni, boş bir Microsoft Azure Otomasyonu runbook oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8451c-108">The **New-AzureAutomationRunbook** cmdlet creates a new, empty Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="8451c-109">Yeni runbook oluşturmak için bir ad belirtin.</span><span class="sxs-lookup"><span data-stu-id="8451c-109">Specify a name to create a new runbook.</span></span>

<span data-ttu-id="8451c-110">Ayrıca, bir runbook içeri aktarmak için Windows PowerShell betik (. ps1) dosyasının yolunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8451c-110">You can also specify the path to a Windows PowerShell script (.ps1 ) file to import a runbook.</span></span>
<span data-ttu-id="8451c-111">İçeri aktarılacak komut dosyası tek bir Windows PowerShell Iş akışı tanımı içermelidir.</span><span class="sxs-lookup"><span data-stu-id="8451c-111">The script to import must contain a single Windows PowerShell Workflow definition.</span></span>
<span data-ttu-id="8451c-112">Bu Windows PowerShell Iş akışının adı, runbook 'un adı olur.</span><span class="sxs-lookup"><span data-stu-id="8451c-112">The name of this Windows PowerShell Workflow becomes the name of the runbook.</span></span>

## <span data-ttu-id="8451c-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8451c-113">EXAMPLES</span></span>

### <span data-ttu-id="8451c-114">Örnek 1: runbook oluşturma</span><span class="sxs-lookup"><span data-stu-id="8451c-114">Example 1: Create a runbook</span></span>
```
PS C:\> New-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02"
```

<span data-ttu-id="8451c-115">Bu komut, Contoso17 adlı Otomasyon hesabında Runbook02 adlı yeni bir runbook oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8451c-115">This command creates a new runbook named Runbook02 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8451c-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8451c-116">PARAMETERS</span></span>

### <span data-ttu-id="8451c-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8451c-117">-AutomationAccountName</span></span>
<span data-ttu-id="8451c-118">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8451c-118">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="8451c-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="8451c-119">-Description</span></span>
<span data-ttu-id="8451c-120">Runbook için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="8451c-120">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="8451c-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="8451c-121">-Name</span></span>
<span data-ttu-id="8451c-122">Runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8451c-122">Specifies the name for the runbook.</span></span>

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

### <span data-ttu-id="8451c-123">-Yol</span><span class="sxs-lookup"><span data-stu-id="8451c-123">-Path</span></span>
<span data-ttu-id="8451c-124">Yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8451c-124">Specifies the path.</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8451c-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="8451c-125">-Profile</span></span>
<span data-ttu-id="8451c-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8451c-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8451c-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="8451c-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8451c-128">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="8451c-128">-Tags</span></span>
<span data-ttu-id="8451c-129">Runbook için Etiketler belirtir.</span><span class="sxs-lookup"><span data-stu-id="8451c-129">Specifies tags for the runbook.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8451c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8451c-130">CommonParameters</span></span>
<span data-ttu-id="8451c-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8451c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8451c-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8451c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8451c-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8451c-133">INPUTS</span></span>

## <span data-ttu-id="8451c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8451c-134">OUTPUTS</span></span>

### <span data-ttu-id="8451c-135">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="8451c-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="8451c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8451c-136">NOTES</span></span>

## <span data-ttu-id="8451c-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8451c-137">RELATED LINKS</span></span>

[<span data-ttu-id="8451c-138">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8451c-138">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="8451c-139">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8451c-139">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="8451c-140">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8451c-140">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="8451c-141">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8451c-141">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="8451c-142">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8451c-142">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


