---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: b05ba189c4b718689f95acac1bfcead84cd3415b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939655"
---
# <span data-ttu-id="030dd-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="030dd-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="030dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="030dd-102">SYNOPSIS</span></span>
<span data-ttu-id="030dd-103">Azure Web uygulamasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="030dd-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="030dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="030dd-104">SYNTAX</span></span>

### <span data-ttu-id="030dd-105">S1</span><span class="sxs-lookup"><span data-stu-id="030dd-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="030dd-106">S2</span><span class="sxs-lookup"><span data-stu-id="030dd-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="030dd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="030dd-107">DESCRIPTION</span></span>
<span data-ttu-id="030dd-108">**Start-AzureRmWebApp** cmdlet 'ı bir Azure Web uygulamasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="030dd-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="030dd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="030dd-109">EXAMPLES</span></span>

### <span data-ttu-id="030dd-110">Örnek 1: Web uygulaması başlatma</span><span class="sxs-lookup"><span data-stu-id="030dd-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="030dd-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoWebApp adlı Web uygulamasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="030dd-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="030dd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="030dd-112">PARAMETERS</span></span>

### <span data-ttu-id="030dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="030dd-113">-DefaultProfile</span></span>
<span data-ttu-id="030dd-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="030dd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="030dd-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="030dd-115">-Name</span></span>
<span data-ttu-id="030dd-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="030dd-116">WebApp Name</span></span>

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

### <span data-ttu-id="030dd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="030dd-117">-ResourceGroupName</span></span>
<span data-ttu-id="030dd-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="030dd-118">Resource Group Name</span></span>

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

### <span data-ttu-id="030dd-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="030dd-119">-WebApp</span></span>
<span data-ttu-id="030dd-120">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="030dd-120">WebApp Object</span></span>

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

### <span data-ttu-id="030dd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="030dd-121">CommonParameters</span></span>
<span data-ttu-id="030dd-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="030dd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="030dd-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="030dd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="030dd-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="030dd-124">INPUTS</span></span>

### <span data-ttu-id="030dd-125">Bölge</span><span class="sxs-lookup"><span data-stu-id="030dd-125">Site</span></span>
<span data-ttu-id="030dd-126">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="030dd-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="030dd-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="030dd-127">OUTPUTS</span></span>

## <span data-ttu-id="030dd-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="030dd-128">NOTES</span></span>

## <span data-ttu-id="030dd-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="030dd-129">RELATED LINKS</span></span>

[<span data-ttu-id="030dd-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="030dd-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="030dd-131">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="030dd-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="030dd-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="030dd-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="030dd-133">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="030dd-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="030dd-134">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="030dd-134">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)

