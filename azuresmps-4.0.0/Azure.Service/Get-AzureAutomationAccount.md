---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 7B2D9768-919B-4F54-BBC7-8882CC2C973A
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9ce55e573881a29291085e9bf25381170bbf052
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106371"
---
# <span data-ttu-id="cabbf-101">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cabbf-101">Get-AzureAutomationAccount</span></span>

## <span data-ttu-id="cabbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cabbf-102">SYNOPSIS</span></span>

<span data-ttu-id="cabbf-103">Azure Otomasyonu hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="cabbf-103">Gets Azure Automation accounts.</span></span>

## <span data-ttu-id="cabbf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cabbf-104">SYNTAX</span></span>

```
Get-AzureAutomationAccount [-Name <String>] [-Location <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="cabbf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cabbf-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="cabbf-106">**Get-AzureAutomationAccount** cmdlet 'i aboneliğiniz Için Microsoft Azure Otomasyon hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="cabbf-106">The **Get-AzureAutomationAccount** cmdlet gets the Microsoft Azure Automation accounts for your subscription.</span></span>
<span data-ttu-id="cabbf-107">Otomasyon hesabı, diğer otomasyon hesaplarının kaynaklarından yalıtılmış olan otomasyon kaynakları için bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="cabbf-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span>
<span data-ttu-id="cabbf-108">Otomasyon kaynakları, runbook 'lar, işler ve varlıklar içerir.</span><span class="sxs-lookup"><span data-stu-id="cabbf-108">Automation resources include runbooks, jobs, and assets.</span></span>

## <span data-ttu-id="cabbf-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cabbf-109">EXAMPLES</span></span>

### <span data-ttu-id="cabbf-110">Örnek 1: Otomasyon hesabı alma</span><span class="sxs-lookup"><span data-stu-id="cabbf-110">Example 1: Get an Automation account</span></span>
```
PS C:\> Get-AzureAutomationAccount -Name "Contoso17"
```

<span data-ttu-id="cabbf-111">Bu komut, Contoso17 adlı Otomasyon hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="cabbf-111">This command gets the Automation account named Contoso17.</span></span>

## <span data-ttu-id="cabbf-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cabbf-112">PARAMETERS</span></span>

### <span data-ttu-id="cabbf-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="cabbf-113">-Location</span></span>
<span data-ttu-id="cabbf-114">Otomasyon hesaplarıyla ilişkili bir Azure konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cabbf-114">Specifies an Azure location associated with Automation accounts.</span></span>

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

### <span data-ttu-id="cabbf-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="cabbf-115">-Name</span></span>
<span data-ttu-id="cabbf-116">Azure Otomasyonu hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cabbf-116">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cabbf-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="cabbf-117">-Profile</span></span>
<span data-ttu-id="cabbf-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cabbf-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cabbf-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="cabbf-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cabbf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cabbf-120">CommonParameters</span></span>
<span data-ttu-id="cabbf-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cabbf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cabbf-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cabbf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cabbf-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cabbf-123">INPUTS</span></span>

## <span data-ttu-id="cabbf-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cabbf-124">OUTPUTS</span></span>

### <span data-ttu-id="cabbf-125">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cabbf-125">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="cabbf-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cabbf-126">NOTES</span></span>

## <span data-ttu-id="cabbf-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cabbf-127">RELATED LINKS</span></span>

[<span data-ttu-id="cabbf-128">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cabbf-128">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)

[<span data-ttu-id="cabbf-129">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cabbf-129">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


