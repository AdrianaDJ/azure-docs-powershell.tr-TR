---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 073c98abe9db8b8a8d52c6d9bb06e64b028d379b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936044"
---
# <span data-ttu-id="d54a2-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d54a2-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="d54a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d54a2-102">SYNOPSIS</span></span>
<span data-ttu-id="d54a2-103">Bir Azure Web uygulamasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="d54a2-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="d54a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d54a2-104">SYNTAX</span></span>

### <span data-ttu-id="d54a2-105">S1</span><span class="sxs-lookup"><span data-stu-id="d54a2-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d54a2-106">S2</span><span class="sxs-lookup"><span data-stu-id="d54a2-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d54a2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d54a2-107">DESCRIPTION</span></span>
<span data-ttu-id="d54a2-108">**Stop-AzWebApp** cmdlet 'ı bir Azure Web uygulamasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="d54a2-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="d54a2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d54a2-109">EXAMPLES</span></span>

### <span data-ttu-id="d54a2-110">Örnek 1: Web uygulamasını durdurma</span><span class="sxs-lookup"><span data-stu-id="d54a2-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="d54a2-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoWebApp adlı Web uygulamasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="d54a2-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d54a2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d54a2-112">PARAMETERS</span></span>

### <span data-ttu-id="d54a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d54a2-113">-DefaultProfile</span></span>
<span data-ttu-id="d54a2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d54a2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d54a2-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d54a2-115">-Name</span></span>
<span data-ttu-id="d54a2-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="d54a2-116">WebApp Name</span></span>

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

### <span data-ttu-id="d54a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d54a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="d54a2-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d54a2-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d54a2-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d54a2-119">-WebApp</span></span>
<span data-ttu-id="d54a2-120">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="d54a2-120">WebApp Object</span></span>

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

### <span data-ttu-id="d54a2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d54a2-121">CommonParameters</span></span>
<span data-ttu-id="d54a2-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d54a2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d54a2-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d54a2-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d54a2-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d54a2-124">INPUTS</span></span>

### <span data-ttu-id="d54a2-125">Bölge</span><span class="sxs-lookup"><span data-stu-id="d54a2-125">Site</span></span>
<span data-ttu-id="d54a2-126">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d54a2-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d54a2-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d54a2-127">OUTPUTS</span></span>

## <span data-ttu-id="d54a2-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d54a2-128">NOTES</span></span>

## <span data-ttu-id="d54a2-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d54a2-129">RELATED LINKS</span></span>

[<span data-ttu-id="d54a2-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d54a2-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="d54a2-131">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d54a2-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="d54a2-132">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d54a2-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="d54a2-133">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d54a2-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="d54a2-134">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d54a2-134">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


