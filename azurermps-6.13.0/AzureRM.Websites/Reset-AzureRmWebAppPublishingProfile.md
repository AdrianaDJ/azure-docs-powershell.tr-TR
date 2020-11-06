---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: 096b062325ddfa12eba1d8c0fe8d6a154c3e77fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590784"
---
# <span data-ttu-id="d9f28-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="d9f28-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="d9f28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9f28-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9f28-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9f28-103">SYNTAX</span></span>

### <span data-ttu-id="d9f28-104">S1</span><span class="sxs-lookup"><span data-stu-id="d9f28-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9f28-105">S2</span><span class="sxs-lookup"><span data-stu-id="d9f28-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9f28-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9f28-106">DESCRIPTION</span></span>
<span data-ttu-id="d9f28-107">**Reset-AzureRmWebAppPublishingProfile** cmdlet 'ı belirtilen Web uygulamasının yayımlama profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="d9f28-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="d9f28-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9f28-108">EXAMPLES</span></span>

### <span data-ttu-id="d9f28-109">2</span><span class="sxs-lookup"><span data-stu-id="d9f28-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="d9f28-110">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp yayımlama profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="d9f28-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d9f28-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9f28-111">PARAMETERS</span></span>

### <span data-ttu-id="d9f28-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f28-112">-DefaultProfile</span></span>
<span data-ttu-id="d9f28-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d9f28-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9f28-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="d9f28-114">-Name</span></span>
<span data-ttu-id="d9f28-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="d9f28-115">WebApp Name</span></span>

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

### <span data-ttu-id="d9f28-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9f28-116">-ResourceGroupName</span></span>
<span data-ttu-id="d9f28-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d9f28-117">Resource Group Name</span></span>

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

### <span data-ttu-id="d9f28-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d9f28-118">-WebApp</span></span>
<span data-ttu-id="d9f28-119">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="d9f28-119">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f28-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f28-120">CommonParameters</span></span>
<span data-ttu-id="d9f28-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9f28-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f28-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9f28-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f28-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9f28-123">INPUTS</span></span>

### <span data-ttu-id="d9f28-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d9f28-124">System.String</span></span>

### <span data-ttu-id="d9f28-125">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="d9f28-125">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="d9f28-126">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d9f28-126">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="d9f28-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9f28-127">OUTPUTS</span></span>

### <span data-ttu-id="d9f28-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d9f28-128">System.String</span></span>

## <span data-ttu-id="d9f28-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9f28-129">NOTES</span></span>

## <span data-ttu-id="d9f28-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9f28-130">RELATED LINKS</span></span>
