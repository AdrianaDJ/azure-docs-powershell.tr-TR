---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
ms.openlocfilehash: d1e4e029676eadec3f793aff99a2d68983891f2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593350"
---
# <span data-ttu-id="94eac-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="94eac-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="94eac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94eac-102">SYNOPSIS</span></span>
<span data-ttu-id="94eac-103">Bir Azure Web uygulamasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="94eac-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94eac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94eac-104">SYNTAX</span></span>

### <span data-ttu-id="94eac-105">S1</span><span class="sxs-lookup"><span data-stu-id="94eac-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94eac-106">S2</span><span class="sxs-lookup"><span data-stu-id="94eac-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94eac-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="94eac-107">DESCRIPTION</span></span>
<span data-ttu-id="94eac-108">**Stop-AzureRmWebApp** cmdlet 'ı bir Azure Web uygulamasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="94eac-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="94eac-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94eac-109">EXAMPLES</span></span>

### <span data-ttu-id="94eac-110">Örnek 1: Web uygulamasını durdurma</span><span class="sxs-lookup"><span data-stu-id="94eac-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="94eac-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoWebApp adlı Web uygulamasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="94eac-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="94eac-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94eac-112">PARAMETERS</span></span>

### <span data-ttu-id="94eac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94eac-113">-DefaultProfile</span></span>
<span data-ttu-id="94eac-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94eac-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94eac-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="94eac-115">-Name</span></span>
<span data-ttu-id="94eac-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="94eac-116">WebApp Name</span></span>

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

### <span data-ttu-id="94eac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94eac-117">-ResourceGroupName</span></span>
<span data-ttu-id="94eac-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="94eac-118">Resource Group Name</span></span>

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

### <span data-ttu-id="94eac-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="94eac-119">-WebApp</span></span>
<span data-ttu-id="94eac-120">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="94eac-120">WebApp Object</span></span>

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

### <span data-ttu-id="94eac-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94eac-121">CommonParameters</span></span>
<span data-ttu-id="94eac-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94eac-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94eac-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94eac-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94eac-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94eac-124">INPUTS</span></span>

### <span data-ttu-id="94eac-125">Bölge</span><span class="sxs-lookup"><span data-stu-id="94eac-125">Site</span></span>
<span data-ttu-id="94eac-126">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="94eac-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="94eac-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94eac-127">OUTPUTS</span></span>

## <span data-ttu-id="94eac-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94eac-128">NOTES</span></span>

## <span data-ttu-id="94eac-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94eac-129">RELATED LINKS</span></span>

[<span data-ttu-id="94eac-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="94eac-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="94eac-131">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="94eac-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="94eac-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="94eac-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="94eac-133">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="94eac-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="94eac-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="94eac-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

