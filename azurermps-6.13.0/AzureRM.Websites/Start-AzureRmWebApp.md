---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
ms.openlocfilehash: 034736bf55eb6dc13f7ba8a51ec57da728733eb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587082"
---
# <span data-ttu-id="291fa-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="291fa-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="291fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="291fa-102">SYNOPSIS</span></span>
<span data-ttu-id="291fa-103">Azure Web uygulamasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="291fa-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="291fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="291fa-104">SYNTAX</span></span>

### <span data-ttu-id="291fa-105">S1</span><span class="sxs-lookup"><span data-stu-id="291fa-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="291fa-106">S2</span><span class="sxs-lookup"><span data-stu-id="291fa-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="291fa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="291fa-107">DESCRIPTION</span></span>
<span data-ttu-id="291fa-108">**Start-AzureRmWebApp** cmdlet 'ı bir Azure Web uygulamasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="291fa-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="291fa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="291fa-109">EXAMPLES</span></span>

### <span data-ttu-id="291fa-110">Örnek 1: Web uygulaması başlatma</span><span class="sxs-lookup"><span data-stu-id="291fa-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="291fa-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoWebApp adlı Web uygulamasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="291fa-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="291fa-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="291fa-112">PARAMETERS</span></span>

### <span data-ttu-id="291fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="291fa-113">-DefaultProfile</span></span>
<span data-ttu-id="291fa-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="291fa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="291fa-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="291fa-115">-Name</span></span>
<span data-ttu-id="291fa-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="291fa-116">WebApp Name</span></span>

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

### <span data-ttu-id="291fa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="291fa-117">-ResourceGroupName</span></span>
<span data-ttu-id="291fa-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="291fa-118">Resource Group Name</span></span>

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

### <span data-ttu-id="291fa-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="291fa-119">-WebApp</span></span>
<span data-ttu-id="291fa-120">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="291fa-120">WebApp Object</span></span>

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

### <span data-ttu-id="291fa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="291fa-121">CommonParameters</span></span>
<span data-ttu-id="291fa-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="291fa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="291fa-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="291fa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="291fa-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="291fa-124">INPUTS</span></span>

### <span data-ttu-id="291fa-125">System. String</span><span class="sxs-lookup"><span data-stu-id="291fa-125">System.String</span></span>

### <span data-ttu-id="291fa-126">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="291fa-126">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="291fa-127">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="291fa-127">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="291fa-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="291fa-128">OUTPUTS</span></span>

### <span data-ttu-id="291fa-129">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="291fa-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="291fa-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="291fa-130">NOTES</span></span>

## <span data-ttu-id="291fa-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="291fa-131">RELATED LINKS</span></span>

[<span data-ttu-id="291fa-132">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="291fa-132">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="291fa-133">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="291fa-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="291fa-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="291fa-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="291fa-135">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="291fa-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="291fa-136">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="291fa-136">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


