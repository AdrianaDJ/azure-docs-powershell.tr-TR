---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73BE191D-816F-4376-8304-B0ABA4163EF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a75016368a770221fd0ab373a4b59c5975ee2a24
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106481"
---
# <span data-ttu-id="20938-101">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="20938-101">Remove-AzureAutomationModule</span></span>

## <span data-ttu-id="20938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20938-102">SYNOPSIS</span></span>

<span data-ttu-id="20938-103">Bir modülü Otomasyon 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="20938-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="20938-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20938-104">SYNTAX</span></span>

```
Remove-AzureAutomationModule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="20938-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="20938-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="20938-106">**Remove-AzureAutomationModule** cmdlet 'ı Microsoft Azure Otomasyonu 'ndan Otomasyon hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="20938-106">The **Remove-AzureAutomationModule** cmdlet removes an Automation account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="20938-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20938-107">EXAMPLES</span></span>

### <span data-ttu-id="20938-108">Örnek 1: modül kaldırma</span><span class="sxs-lookup"><span data-stu-id="20938-108">Example 1: Remove a module</span></span>
```
PS C:\> Remove-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="20938-109">Bu komut, Contoso17 adlı Otomasyon hesabından ContosoModule adlı bir modülü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="20938-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="20938-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20938-110">PARAMETERS</span></span>

### <span data-ttu-id="20938-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="20938-111">-AutomationAccountName</span></span>
<span data-ttu-id="20938-112">Modüle sahip otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="20938-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="20938-113">-Force</span><span class="sxs-lookup"><span data-stu-id="20938-113">-Force</span></span>
<span data-ttu-id="20938-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="20938-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20938-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="20938-115">-Name</span></span>
<span data-ttu-id="20938-116">Kaldırılacak modülün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="20938-116">Specifies the name of the module to remove.</span></span>

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

### <span data-ttu-id="20938-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="20938-117">-Profile</span></span>
<span data-ttu-id="20938-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="20938-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20938-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="20938-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="20938-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20938-120">CommonParameters</span></span>
<span data-ttu-id="20938-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20938-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20938-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20938-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20938-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20938-123">INPUTS</span></span>

## <span data-ttu-id="20938-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20938-124">OUTPUTS</span></span>

## <span data-ttu-id="20938-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20938-125">NOTES</span></span>

## <span data-ttu-id="20938-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20938-126">RELATED LINKS</span></span>

[<span data-ttu-id="20938-127">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="20938-127">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="20938-128">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="20938-128">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="20938-129">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="20938-129">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


