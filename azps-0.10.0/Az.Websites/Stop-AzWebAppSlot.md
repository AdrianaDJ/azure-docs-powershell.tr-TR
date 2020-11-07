---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: 4ac4482cb5972553b1dad3972200d2f0eb032fe4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936046"
---
# <span data-ttu-id="dc58a-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc58a-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="dc58a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc58a-102">SYNOPSIS</span></span>
<span data-ttu-id="dc58a-103">Azure Web App yuvasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="dc58a-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="dc58a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc58a-104">SYNTAX</span></span>

### <span data-ttu-id="dc58a-105">S1</span><span class="sxs-lookup"><span data-stu-id="dc58a-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc58a-106">S2</span><span class="sxs-lookup"><span data-stu-id="dc58a-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc58a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc58a-107">DESCRIPTION</span></span>
<span data-ttu-id="dc58a-108">**Stop-AzWebAppSlot** cmdlet 'ı bir Azure Web App yuvasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="dc58a-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="dc58a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc58a-109">EXAMPLES</span></span>

### <span data-ttu-id="dc58a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dc58a-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="dc58a-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoWebApp adlı Web uygulamasının bulunduğu yuva Slot001.</span><span class="sxs-lookup"><span data-stu-id="dc58a-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="dc58a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc58a-112">PARAMETERS</span></span>

### <span data-ttu-id="dc58a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc58a-113">-DefaultProfile</span></span>
<span data-ttu-id="dc58a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dc58a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc58a-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="dc58a-115">-Name</span></span>
<span data-ttu-id="dc58a-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="dc58a-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc58a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc58a-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc58a-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="dc58a-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc58a-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="dc58a-119">-Slot</span></span>
<span data-ttu-id="dc58a-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="dc58a-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc58a-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="dc58a-121">-WebApp</span></span>
<span data-ttu-id="dc58a-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="dc58a-122">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc58a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc58a-123">CommonParameters</span></span>
<span data-ttu-id="dc58a-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc58a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc58a-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc58a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc58a-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc58a-126">INPUTS</span></span>

### <span data-ttu-id="dc58a-127">Bölge</span><span class="sxs-lookup"><span data-stu-id="dc58a-127">Site</span></span>
<span data-ttu-id="dc58a-128">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="dc58a-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="dc58a-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc58a-129">OUTPUTS</span></span>

## <span data-ttu-id="dc58a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc58a-130">NOTES</span></span>

## <span data-ttu-id="dc58a-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc58a-131">RELATED LINKS</span></span>

