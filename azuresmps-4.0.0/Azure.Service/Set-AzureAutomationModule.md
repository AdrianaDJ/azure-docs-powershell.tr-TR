---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 9CED6E53-B65C-4D55-8AC7-9E8A8B143544
online version: ''
schema: 2.0.0
ms.openlocfilehash: da8f0e3bdc9e1cf573e9189e49feda85ee8c1b90
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105830"
---
# <span data-ttu-id="b589c-101">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="b589c-101">Set-AzureAutomationModule</span></span>

## <span data-ttu-id="b589c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b589c-102">SYNOPSIS</span></span>

<span data-ttu-id="b589c-103">Otomasyon 'da bir modülü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b589c-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="b589c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b589c-104">SYNTAX</span></span>

```
Set-AzureAutomationModule -Name <String> [-Tags <IDictionary>] [-ContentLinkUri <Uri>]
 [-ContentLinkVersion <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b589c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b589c-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="b589c-106">**Set-AzureAutomationModule** cmdlet 'i modülün yeni bir sürümünü içeri aktarır veya Azure Otomasyonu 'ndaki modülün yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b589c-106">The **Set-AzureAutomationModule** cmdlet imports a new version of a module or changes the configuration of the module in Azure Automation.</span></span>

## <span data-ttu-id="b589c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b589c-107">EXAMPLES</span></span>

### <span data-ttu-id="b589c-108">Örnek 1: modül güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b589c-108">Example 1: Update a module</span></span>
```
PS C:\> Set-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1"
```

<span data-ttu-id="b589c-109">Bu komut, Contoso17 adlı Azure Otomasyonu hesabına ContosoModule adlı var olan bir modülün güncelleştirilmiş sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="b589c-109">This command imports an updated version of an existing module named ContosoModule into the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="b589c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b589c-110">PARAMETERS</span></span>

### <span data-ttu-id="b589c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b589c-111">-AutomationAccountName</span></span>
<span data-ttu-id="b589c-112">Modüle sahip otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b589c-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="b589c-113">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="b589c-113">-ContentLinkUri</span></span>
<span data-ttu-id="b589c-114">Modül dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b589c-114">Specifies the path to the module file.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b589c-115">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="b589c-115">-ContentLinkVersion</span></span>
<span data-ttu-id="b589c-116">Modülün sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b589c-116">Specifies the version of the module.</span></span>

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

### <span data-ttu-id="b589c-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="b589c-117">-Name</span></span>
<span data-ttu-id="b589c-118">Modülün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b589c-118">Specifies the name of the module.</span></span>

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

### <span data-ttu-id="b589c-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="b589c-119">-Profile</span></span>
<span data-ttu-id="b589c-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b589c-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b589c-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b589c-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b589c-122">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="b589c-122">-Tags</span></span>
<span data-ttu-id="b589c-123">Modül için Etiketler belirtir.</span><span class="sxs-lookup"><span data-stu-id="b589c-123">Specifies tags for the module.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b589c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b589c-124">CommonParameters</span></span>
<span data-ttu-id="b589c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b589c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b589c-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b589c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b589c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b589c-127">INPUTS</span></span>

### <span data-ttu-id="b589c-128">Microsoft. Azure. Commands. Automation. model. Module</span><span class="sxs-lookup"><span data-stu-id="b589c-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="b589c-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b589c-129">OUTPUTS</span></span>

## <span data-ttu-id="b589c-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b589c-130">NOTES</span></span>

## <span data-ttu-id="b589c-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b589c-131">RELATED LINKS</span></span>

[<span data-ttu-id="b589c-132">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="b589c-132">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="b589c-133">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="b589c-133">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="b589c-134">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="b589c-134">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)


