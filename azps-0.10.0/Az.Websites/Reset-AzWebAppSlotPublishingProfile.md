---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/reset-Azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: ec0b95ffee67d5597a06ed0729cded33e7489465
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936078"
---
# <span data-ttu-id="6240b-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="6240b-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="6240b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6240b-102">SYNOPSIS</span></span>

## <span data-ttu-id="6240b-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6240b-103">SYNTAX</span></span>

### <span data-ttu-id="6240b-104">S1</span><span class="sxs-lookup"><span data-stu-id="6240b-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6240b-105">S2</span><span class="sxs-lookup"><span data-stu-id="6240b-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6240b-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="6240b-106">DESCRIPTION</span></span>
<span data-ttu-id="6240b-107">**Reset-AzWebAppSlotPublishingProfile** cmdlet 'i, belirtilen Web uygulaması yuvasının yayımlama profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="6240b-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="6240b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6240b-108">EXAMPLES</span></span>

### <span data-ttu-id="6240b-109">2</span><span class="sxs-lookup"><span data-stu-id="6240b-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="6240b-110">Bu komut, Default-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp için slot001 adındaki yuva profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="6240b-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="6240b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6240b-111">PARAMETERS</span></span>

### <span data-ttu-id="6240b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6240b-112">-DefaultProfile</span></span>
<span data-ttu-id="6240b-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6240b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6240b-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="6240b-114">-Name</span></span>
<span data-ttu-id="6240b-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="6240b-115">WebApp Name</span></span>

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

### <span data-ttu-id="6240b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6240b-116">-ResourceGroupName</span></span>
<span data-ttu-id="6240b-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6240b-117">Resource Group Name</span></span>

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

### <span data-ttu-id="6240b-118">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="6240b-118">-Slot</span></span>
<span data-ttu-id="6240b-119">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="6240b-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="6240b-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6240b-120">-WebApp</span></span>
<span data-ttu-id="6240b-121">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="6240b-121">WebApp Object</span></span>

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

### <span data-ttu-id="6240b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6240b-122">CommonParameters</span></span>
<span data-ttu-id="6240b-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6240b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6240b-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6240b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6240b-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6240b-125">INPUTS</span></span>

### <span data-ttu-id="6240b-126">Bölge</span><span class="sxs-lookup"><span data-stu-id="6240b-126">Site</span></span>
<span data-ttu-id="6240b-127">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6240b-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6240b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6240b-128">OUTPUTS</span></span>

## <span data-ttu-id="6240b-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6240b-129">NOTES</span></span>

## <span data-ttu-id="6240b-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6240b-130">RELATED LINKS</span></span>

