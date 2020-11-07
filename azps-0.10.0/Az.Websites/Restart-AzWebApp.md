---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restart-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: 975b49af1e20c5b9f4839a561494eaeb8275f02f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936067"
---
# <span data-ttu-id="cac22-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cac22-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="cac22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cac22-102">SYNOPSIS</span></span>
<span data-ttu-id="cac22-103">Bir Azure Web uygulamasını yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="cac22-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="cac22-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cac22-104">SYNTAX</span></span>

### <span data-ttu-id="cac22-105">S1</span><span class="sxs-lookup"><span data-stu-id="cac22-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cac22-106">S2</span><span class="sxs-lookup"><span data-stu-id="cac22-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cac22-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cac22-107">DESCRIPTION</span></span>
<span data-ttu-id="cac22-108">**Restart-AzWebApp** cmdlet 'i durur ve bir Azure Web uygulamasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="cac22-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="cac22-109">Web uygulaması durdurulmuş durumdaysa, Start-AzWebApp cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cac22-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="cac22-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cac22-110">EXAMPLES</span></span>

### <span data-ttu-id="cac22-111">Örnek 1: Web uygulamasını yeniden başlatma</span><span class="sxs-lookup"><span data-stu-id="cac22-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="cac22-112">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoSite adlı Azure Web uygulamasını durdurur ve sonra yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="cac22-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="cac22-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cac22-113">PARAMETERS</span></span>

### <span data-ttu-id="cac22-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cac22-114">-DefaultProfile</span></span>
<span data-ttu-id="cac22-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cac22-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cac22-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="cac22-116">-Name</span></span>
<span data-ttu-id="cac22-117">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="cac22-117">WebApp Name</span></span>

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

### <span data-ttu-id="cac22-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cac22-118">-ResourceGroupName</span></span>
<span data-ttu-id="cac22-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="cac22-119">Resource Group Name</span></span>

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

### <span data-ttu-id="cac22-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cac22-120">-WebApp</span></span>
<span data-ttu-id="cac22-121">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="cac22-121">WebApp Object</span></span>

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

### <span data-ttu-id="cac22-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac22-122">CommonParameters</span></span>
<span data-ttu-id="cac22-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cac22-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac22-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cac22-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac22-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cac22-125">INPUTS</span></span>

### <span data-ttu-id="cac22-126">Bölge</span><span class="sxs-lookup"><span data-stu-id="cac22-126">Site</span></span>
<span data-ttu-id="cac22-127">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="cac22-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="cac22-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cac22-128">OUTPUTS</span></span>

## <span data-ttu-id="cac22-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cac22-129">NOTES</span></span>

## <span data-ttu-id="cac22-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cac22-130">RELATED LINKS</span></span>

[<span data-ttu-id="cac22-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cac22-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="cac22-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cac22-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="cac22-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cac22-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="cac22-134">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cac22-134">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="cac22-135">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cac22-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


