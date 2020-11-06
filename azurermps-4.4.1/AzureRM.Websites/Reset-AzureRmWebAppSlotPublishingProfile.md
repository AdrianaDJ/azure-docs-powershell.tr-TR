---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: b6a01079bed80017054e7fe52673012827dce02d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586870"
---
# <span data-ttu-id="62e40-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="62e40-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="62e40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62e40-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62e40-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62e40-103">SYNTAX</span></span>

### <span data-ttu-id="62e40-104">S1</span><span class="sxs-lookup"><span data-stu-id="62e40-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62e40-105">S2</span><span class="sxs-lookup"><span data-stu-id="62e40-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62e40-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="62e40-106">DESCRIPTION</span></span>
<span data-ttu-id="62e40-107">**Reset-AzureRmWebAppSlotPublishingProfile** cmdlet 'ı belirtilen Web App yuvasının yayımlama profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="62e40-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="62e40-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62e40-108">EXAMPLES</span></span>

### <span data-ttu-id="62e40-109">2</span><span class="sxs-lookup"><span data-stu-id="62e40-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="62e40-110">Bu komut, Default-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp için slot001 adındaki yuva profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="62e40-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="62e40-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62e40-111">PARAMETERS</span></span>

### <span data-ttu-id="62e40-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="62e40-112">-Name</span></span>
<span data-ttu-id="62e40-113">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="62e40-113">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e40-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e40-114">-ResourceGroupName</span></span>
<span data-ttu-id="62e40-115">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="62e40-115">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e40-116">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="62e40-116">-Slot</span></span>
<span data-ttu-id="62e40-117">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="62e40-117">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e40-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="62e40-118">-WebApp</span></span>
<span data-ttu-id="62e40-119">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="62e40-119">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62e40-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e40-120">-DefaultProfile</span></span>
<span data-ttu-id="62e40-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="62e40-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e40-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e40-122">CommonParameters</span></span>
<span data-ttu-id="62e40-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62e40-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e40-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62e40-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e40-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62e40-125">INPUTS</span></span>

### <span data-ttu-id="62e40-126">Bölge</span><span class="sxs-lookup"><span data-stu-id="62e40-126">Site</span></span>
<span data-ttu-id="62e40-127">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="62e40-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="62e40-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62e40-128">OUTPUTS</span></span>

## <span data-ttu-id="62e40-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62e40-129">NOTES</span></span>

## <span data-ttu-id="62e40-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62e40-130">RELATED LINKS</span></span>

