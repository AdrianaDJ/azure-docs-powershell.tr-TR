---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 33fdfdc1c8b0c4b7bfddbc6b0aafd9ab38ffe701
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098067"
---
# <span data-ttu-id="38fee-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="38fee-101">Start-AzWebApp</span></span>

## <span data-ttu-id="38fee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38fee-102">SYNOPSIS</span></span>
<span data-ttu-id="38fee-103">Azure Web uygulamasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="38fee-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="38fee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38fee-104">SYNTAX</span></span>

### <span data-ttu-id="38fee-105">S1</span><span class="sxs-lookup"><span data-stu-id="38fee-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38fee-106">S2</span><span class="sxs-lookup"><span data-stu-id="38fee-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38fee-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="38fee-107">DESCRIPTION</span></span>
<span data-ttu-id="38fee-108">**Start-AzWebApp** cmdlet 'ı bir Azure Web uygulamasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="38fee-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="38fee-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38fee-109">EXAMPLES</span></span>

### <span data-ttu-id="38fee-110">Örnek 1: Web uygulaması başlatma</span><span class="sxs-lookup"><span data-stu-id="38fee-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="38fee-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoWebApp adlı Web uygulamasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="38fee-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="38fee-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38fee-112">PARAMETERS</span></span>

### <span data-ttu-id="38fee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38fee-113">-DefaultProfile</span></span>
<span data-ttu-id="38fee-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38fee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38fee-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="38fee-115">-Name</span></span>
<span data-ttu-id="38fee-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="38fee-116">WebApp Name</span></span>

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

### <span data-ttu-id="38fee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38fee-117">-ResourceGroupName</span></span>
<span data-ttu-id="38fee-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="38fee-118">Resource Group Name</span></span>

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

### <span data-ttu-id="38fee-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="38fee-119">-WebApp</span></span>
<span data-ttu-id="38fee-120">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="38fee-120">WebApp Object</span></span>

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

### <span data-ttu-id="38fee-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38fee-121">CommonParameters</span></span>
<span data-ttu-id="38fee-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38fee-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38fee-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38fee-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38fee-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38fee-124">INPUTS</span></span>

### <span data-ttu-id="38fee-125">System. String</span><span class="sxs-lookup"><span data-stu-id="38fee-125">System.String</span></span>

### <span data-ttu-id="38fee-126">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="38fee-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="38fee-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38fee-127">OUTPUTS</span></span>

### <span data-ttu-id="38fee-128">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="38fee-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="38fee-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38fee-129">NOTES</span></span>

## <span data-ttu-id="38fee-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38fee-130">RELATED LINKS</span></span>

[<span data-ttu-id="38fee-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="38fee-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="38fee-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="38fee-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="38fee-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="38fee-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="38fee-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="38fee-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="38fee-135">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="38fee-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


