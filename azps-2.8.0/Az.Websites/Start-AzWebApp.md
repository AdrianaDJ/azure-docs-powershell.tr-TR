---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 09c618e617775e0c2bfffab1794f2427f97d811c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934470"
---
# <span data-ttu-id="205b5-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="205b5-101">Start-AzWebApp</span></span>

## <span data-ttu-id="205b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="205b5-102">SYNOPSIS</span></span>
<span data-ttu-id="205b5-103">Azure Web uygulamasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="205b5-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="205b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="205b5-104">SYNTAX</span></span>

### <span data-ttu-id="205b5-105">S1</span><span class="sxs-lookup"><span data-stu-id="205b5-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="205b5-106">S2</span><span class="sxs-lookup"><span data-stu-id="205b5-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="205b5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="205b5-107">DESCRIPTION</span></span>
<span data-ttu-id="205b5-108">**Start-AzWebApp** cmdlet 'ı bir Azure Web uygulamasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="205b5-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="205b5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="205b5-109">EXAMPLES</span></span>

### <span data-ttu-id="205b5-110">Örnek 1: Web uygulaması başlatma</span><span class="sxs-lookup"><span data-stu-id="205b5-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="205b5-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoWebApp adlı Web uygulamasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="205b5-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="205b5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="205b5-112">PARAMETERS</span></span>

### <span data-ttu-id="205b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="205b5-113">-DefaultProfile</span></span>
<span data-ttu-id="205b5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="205b5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="205b5-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="205b5-115">-Name</span></span>
<span data-ttu-id="205b5-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="205b5-116">WebApp Name</span></span>

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

### <span data-ttu-id="205b5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="205b5-117">-ResourceGroupName</span></span>
<span data-ttu-id="205b5-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="205b5-118">Resource Group Name</span></span>

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

### <span data-ttu-id="205b5-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="205b5-119">-WebApp</span></span>
<span data-ttu-id="205b5-120">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="205b5-120">WebApp Object</span></span>

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

### <span data-ttu-id="205b5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205b5-121">CommonParameters</span></span>
<span data-ttu-id="205b5-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="205b5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205b5-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="205b5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205b5-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="205b5-124">INPUTS</span></span>

### <span data-ttu-id="205b5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="205b5-125">System.String</span></span>

### <span data-ttu-id="205b5-126">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="205b5-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="205b5-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="205b5-127">OUTPUTS</span></span>

### <span data-ttu-id="205b5-128">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="205b5-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="205b5-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="205b5-129">NOTES</span></span>

## <span data-ttu-id="205b5-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="205b5-130">RELATED LINKS</span></span>

[<span data-ttu-id="205b5-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="205b5-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="205b5-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="205b5-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="205b5-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="205b5-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="205b5-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="205b5-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="205b5-135">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="205b5-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


