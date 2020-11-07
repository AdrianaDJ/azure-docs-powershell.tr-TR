---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: eb1f96eaf85e6a5e7234e09c319b2e0c1117d456
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938752"
---
# <span data-ttu-id="3beff-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3beff-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="3beff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3beff-102">SYNOPSIS</span></span>
<span data-ttu-id="3beff-103">Belirtilen kaynak grubundaki Azure Web uygulamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="3beff-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3beff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3beff-104">SYNTAX</span></span>

### <span data-ttu-id="3beff-105">S1</span><span class="sxs-lookup"><span data-stu-id="3beff-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3beff-106">S2</span><span class="sxs-lookup"><span data-stu-id="3beff-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3beff-107">S3</span><span class="sxs-lookup"><span data-stu-id="3beff-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3beff-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3beff-108">DESCRIPTION</span></span>
<span data-ttu-id="3beff-109">**Get-AzureRmWebApp** cmdlet 'ı bir Azure Web App hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="3beff-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="3beff-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3beff-110">EXAMPLES</span></span>

### <span data-ttu-id="3beff-111">Örnek 1: kaynak grubundan Web uygulaması alma</span><span class="sxs-lookup"><span data-stu-id="3beff-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="3beff-112">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan ContosoSite adlı Web uygulamasını alır.</span><span class="sxs-lookup"><span data-stu-id="3beff-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="3beff-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3beff-113">PARAMETERS</span></span>

### <span data-ttu-id="3beff-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3beff-114">-AppServicePlan</span></span>
<span data-ttu-id="3beff-115">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="3beff-115">App Service Plan object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3beff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3beff-116">-DefaultProfile</span></span>
<span data-ttu-id="3beff-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3beff-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3beff-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="3beff-118">-Location</span></span>
<span data-ttu-id="3beff-119">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="3beff-119">Location</span></span>

```yaml
Type: String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3beff-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="3beff-120">-Name</span></span>
<span data-ttu-id="3beff-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="3beff-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3beff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3beff-122">-ResourceGroupName</span></span>
<span data-ttu-id="3beff-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="3beff-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3beff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3beff-124">CommonParameters</span></span>
<span data-ttu-id="3beff-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3beff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3beff-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3beff-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3beff-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3beff-127">INPUTS</span></span>

### <span data-ttu-id="3beff-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3beff-128">System.String</span></span>

## <span data-ttu-id="3beff-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3beff-129">OUTPUTS</span></span>

### <span data-ttu-id="3beff-130">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="3beff-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="3beff-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3beff-131">NOTES</span></span>

## <span data-ttu-id="3beff-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3beff-132">RELATED LINKS</span></span>

[<span data-ttu-id="3beff-133">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3beff-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="3beff-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3beff-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="3beff-135">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3beff-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="3beff-136">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3beff-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="3beff-137">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3beff-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


