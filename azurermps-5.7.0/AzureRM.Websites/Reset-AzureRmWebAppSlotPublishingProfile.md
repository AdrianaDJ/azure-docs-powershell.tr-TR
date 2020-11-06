---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: 352b0bc196745aba3c5eeda357e0727a9ea3e4c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591526"
---
# <span data-ttu-id="5aa47-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="5aa47-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="5aa47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5aa47-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5aa47-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5aa47-103">SYNTAX</span></span>

### <span data-ttu-id="5aa47-104">S1</span><span class="sxs-lookup"><span data-stu-id="5aa47-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5aa47-105">S2</span><span class="sxs-lookup"><span data-stu-id="5aa47-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5aa47-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="5aa47-106">DESCRIPTION</span></span>
<span data-ttu-id="5aa47-107">**Reset-AzureRmWebAppSlotPublishingProfile** cmdlet 'ı belirtilen Web App yuvasının yayımlama profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="5aa47-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="5aa47-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5aa47-108">EXAMPLES</span></span>

### <span data-ttu-id="5aa47-109">2</span><span class="sxs-lookup"><span data-stu-id="5aa47-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="5aa47-110">Bu komut, Default-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp için slot001 adındaki yuva profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="5aa47-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="5aa47-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5aa47-111">PARAMETERS</span></span>

### <span data-ttu-id="5aa47-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aa47-112">-DefaultProfile</span></span>
<span data-ttu-id="5aa47-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5aa47-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa47-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="5aa47-114">-Name</span></span>
<span data-ttu-id="5aa47-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="5aa47-115">WebApp Name</span></span>

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

### <span data-ttu-id="5aa47-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aa47-116">-ResourceGroupName</span></span>
<span data-ttu-id="5aa47-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5aa47-117">Resource Group Name</span></span>

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

### <span data-ttu-id="5aa47-118">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="5aa47-118">-Slot</span></span>
<span data-ttu-id="5aa47-119">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="5aa47-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="5aa47-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5aa47-120">-WebApp</span></span>
<span data-ttu-id="5aa47-121">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="5aa47-121">WebApp Object</span></span>

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

### <span data-ttu-id="5aa47-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aa47-122">CommonParameters</span></span>
<span data-ttu-id="5aa47-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5aa47-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aa47-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aa47-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aa47-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5aa47-125">INPUTS</span></span>

### <span data-ttu-id="5aa47-126">Bölge</span><span class="sxs-lookup"><span data-stu-id="5aa47-126">Site</span></span>
<span data-ttu-id="5aa47-127">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="5aa47-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5aa47-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5aa47-128">OUTPUTS</span></span>

## <span data-ttu-id="5aa47-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5aa47-129">NOTES</span></span>

## <span data-ttu-id="5aa47-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5aa47-130">RELATED LINKS</span></span>

