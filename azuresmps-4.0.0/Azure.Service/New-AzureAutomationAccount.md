---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 59CDE74B-EFB3-4904-A482-466B0EA17F4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a787193669cab32a43b7c9b9eb2010a6e545539b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106224"
---
# <span data-ttu-id="ec8af-101">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ec8af-101">New-AzureAutomationAccount</span></span>

## <span data-ttu-id="ec8af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec8af-102">SYNOPSIS</span></span>

<span data-ttu-id="ec8af-103">Otomasyon hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec8af-103">Creates an Automation account.</span></span>

## <span data-ttu-id="ec8af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec8af-104">SYNTAX</span></span>

```
New-AzureAutomationAccount -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ec8af-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec8af-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ec8af-106">**New-AzureAutomationAccount** cmdlet 'ı Microsoft Azure Otomasyonu 'nda yeni bir hesap oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec8af-106">The **New-AzureAutomationAccount** cmdlet creates a new account in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="ec8af-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec8af-107">EXAMPLES</span></span>

### <span data-ttu-id="ec8af-108">Örnek 1: Otomasyon hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ec8af-108">Example 1: Create an Automation account</span></span>
```
PS C:\> New-AzureAutomationAccount -Name "MyAutomationAccount" -Location "East US"
```

<span data-ttu-id="ec8af-109">Bu komut, Doğu ABD bölgesindeki MyAutomationAccount adlı bir Otomasyon hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec8af-109">This command creates an Automation account named MyAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="ec8af-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec8af-110">PARAMETERS</span></span>

### <span data-ttu-id="ec8af-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="ec8af-111">-Location</span></span>
<span data-ttu-id="ec8af-112">Hesabın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec8af-112">Specifies the location of the account.</span></span>

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

### <span data-ttu-id="ec8af-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec8af-113">-Name</span></span>
<span data-ttu-id="ec8af-114">Hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec8af-114">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8af-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="ec8af-115">-Profile</span></span>
<span data-ttu-id="ec8af-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec8af-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec8af-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ec8af-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec8af-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec8af-118">CommonParameters</span></span>
<span data-ttu-id="ec8af-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec8af-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec8af-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec8af-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec8af-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec8af-121">INPUTS</span></span>

## <span data-ttu-id="ec8af-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec8af-122">OUTPUTS</span></span>

### <span data-ttu-id="ec8af-123">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ec8af-123">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="ec8af-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec8af-124">NOTES</span></span>

## <span data-ttu-id="ec8af-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec8af-125">RELATED LINKS</span></span>

[<span data-ttu-id="ec8af-126">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ec8af-126">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="ec8af-127">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ec8af-127">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


