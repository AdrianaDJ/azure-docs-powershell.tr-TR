---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: 775c82585d31e223b3f769cccc458e1523f42b62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939825"
---
# <span data-ttu-id="fef07-101">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fef07-101">Restart-AzureRmWebApp</span></span>

## <span data-ttu-id="fef07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fef07-102">SYNOPSIS</span></span>
<span data-ttu-id="fef07-103">Bir Azure Web uygulamasını yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="fef07-103">Restarts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fef07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fef07-104">SYNTAX</span></span>

### <span data-ttu-id="fef07-105">S1</span><span class="sxs-lookup"><span data-stu-id="fef07-105">S1</span></span>
```
Restart-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fef07-106">S2</span><span class="sxs-lookup"><span data-stu-id="fef07-106">S2</span></span>
```
Restart-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fef07-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fef07-107">DESCRIPTION</span></span>
<span data-ttu-id="fef07-108">**Restart-AzureRmWebApp** cmdlet 'i durur ve bir Azure Web uygulamasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="fef07-108">The **Restart-AzureRmWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="fef07-109">Web uygulaması durdurulmuş durumdaysa, Start-AzureRmWebApp cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fef07-109">If the Web App is in a stopped state, use the Start-AzureRmWebApp cmdlet.</span></span>

## <span data-ttu-id="fef07-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fef07-110">EXAMPLES</span></span>

### <span data-ttu-id="fef07-111">Örnek 1: Web uygulamasını yeniden başlatma</span><span class="sxs-lookup"><span data-stu-id="fef07-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="fef07-112">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoSite adlı Azure Web uygulamasını durdurur ve sonra yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="fef07-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="fef07-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fef07-113">PARAMETERS</span></span>

### <span data-ttu-id="fef07-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef07-114">-DefaultProfile</span></span>
<span data-ttu-id="fef07-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fef07-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fef07-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="fef07-116">-Name</span></span>
<span data-ttu-id="fef07-117">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="fef07-117">WebApp Name</span></span>

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

### <span data-ttu-id="fef07-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fef07-118">-ResourceGroupName</span></span>
<span data-ttu-id="fef07-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="fef07-119">Resource Group Name</span></span>

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

### <span data-ttu-id="fef07-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fef07-120">-WebApp</span></span>
<span data-ttu-id="fef07-121">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="fef07-121">WebApp Object</span></span>

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

### <span data-ttu-id="fef07-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef07-122">CommonParameters</span></span>
<span data-ttu-id="fef07-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fef07-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef07-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fef07-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef07-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fef07-125">INPUTS</span></span>

### <span data-ttu-id="fef07-126">Bölge</span><span class="sxs-lookup"><span data-stu-id="fef07-126">Site</span></span>
<span data-ttu-id="fef07-127">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fef07-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="fef07-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fef07-128">OUTPUTS</span></span>

## <span data-ttu-id="fef07-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fef07-129">NOTES</span></span>

## <span data-ttu-id="fef07-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fef07-130">RELATED LINKS</span></span>

[<span data-ttu-id="fef07-131">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fef07-131">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="fef07-132">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fef07-132">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="fef07-133">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fef07-133">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="fef07-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fef07-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="fef07-135">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fef07-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)

