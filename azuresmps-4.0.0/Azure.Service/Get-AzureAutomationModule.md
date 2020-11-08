---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73F90276-FABD-414A-B29D-83F371C1ED21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0544b4d5fafcb388b65271e736f43a15f02980c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106368"
---
# <span data-ttu-id="93f5e-101">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="93f5e-101">Get-AzureAutomationModule</span></span>

## <span data-ttu-id="93f5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93f5e-102">SYNOPSIS</span></span>

<span data-ttu-id="93f5e-103">Bir Azure Otomasyonu modülü edinin.</span><span class="sxs-lookup"><span data-stu-id="93f5e-103">Get an Azure Automation module.</span></span>

## <span data-ttu-id="93f5e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93f5e-104">SYNTAX</span></span>

### <span data-ttu-id="93f5e-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="93f5e-105">ByAll (Default)</span></span>
```
Get-AzureAutomationModule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="93f5e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="93f5e-106">ByName</span></span>
```
Get-AzureAutomationModule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="93f5e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="93f5e-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="93f5e-108">**Get-AzureAutomationModule** cmdlet 'i bir veya daha fazla Microsoft Azure Automation modülünü alır.</span><span class="sxs-lookup"><span data-stu-id="93f5e-108">The **Get-AzureAutomationModule** cmdlet gets one or more Microsoft Azure Automation modules.</span></span>
<span data-ttu-id="93f5e-109">Varsayılan olarak, tüm modüller döndürülür.</span><span class="sxs-lookup"><span data-stu-id="93f5e-109">By default, all modules are returned.</span></span>
<span data-ttu-id="93f5e-110">Belirli bir modül edinmek için adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="93f5e-110">To get a specific module, specify its name.</span></span>

## <span data-ttu-id="93f5e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93f5e-111">EXAMPLES</span></span>

### <span data-ttu-id="93f5e-112">Örnek 1: tüm modülleri al</span><span class="sxs-lookup"><span data-stu-id="93f5e-112">Example 1: Get all modules</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17"
```

<span data-ttu-id="93f5e-113">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki tüm modülleri alır.</span><span class="sxs-lookup"><span data-stu-id="93f5e-113">This command gets all modules in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="93f5e-114">Örnek 2: modül alma</span><span class="sxs-lookup"><span data-stu-id="93f5e-114">Example 2: Get a module</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="93f5e-115">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki ContosoModule adlı bir modül alır.</span><span class="sxs-lookup"><span data-stu-id="93f5e-115">This command gets a module named ContosoModule in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="93f5e-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93f5e-116">PARAMETERS</span></span>

### <span data-ttu-id="93f5e-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="93f5e-117">-AutomationAccountName</span></span>
<span data-ttu-id="93f5e-118">Alınacak runbook ile otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93f5e-118">Specifies the name of the Automation account with the runbook to retrieve.</span></span>

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

### <span data-ttu-id="93f5e-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="93f5e-119">-Name</span></span>
<span data-ttu-id="93f5e-120">Alınacak modülün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93f5e-120">Specifies the name of a module to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93f5e-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="93f5e-121">-Profile</span></span>
<span data-ttu-id="93f5e-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="93f5e-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93f5e-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="93f5e-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="93f5e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f5e-124">CommonParameters</span></span>
<span data-ttu-id="93f5e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93f5e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f5e-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93f5e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f5e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93f5e-127">INPUTS</span></span>

## <span data-ttu-id="93f5e-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93f5e-128">OUTPUTS</span></span>

### <span data-ttu-id="93f5e-129">Microsoft. Azure. Commands. Automation. model. Module</span><span class="sxs-lookup"><span data-stu-id="93f5e-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="93f5e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93f5e-130">NOTES</span></span>

## <span data-ttu-id="93f5e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93f5e-131">RELATED LINKS</span></span>

[<span data-ttu-id="93f5e-132">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="93f5e-132">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="93f5e-133">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="93f5e-133">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="93f5e-134">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="93f5e-134">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


