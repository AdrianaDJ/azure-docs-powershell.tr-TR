---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 64945cf503248fc0561dc894090c73d2d7151e4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763076"
---
# <span data-ttu-id="95313-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="95313-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="95313-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95313-102">SYNOPSIS</span></span>
<span data-ttu-id="95313-103">Belirtilen kaynak grubundaki Azure Web uygulamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="95313-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95313-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95313-104">SYNTAX</span></span>

### <span data-ttu-id="95313-105">S1</span><span class="sxs-lookup"><span data-stu-id="95313-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95313-106">S2</span><span class="sxs-lookup"><span data-stu-id="95313-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95313-107">S3</span><span class="sxs-lookup"><span data-stu-id="95313-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95313-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="95313-108">DESCRIPTION</span></span>
<span data-ttu-id="95313-109">**Get-AzureRmWebApp** cmdlet 'ı bir Azure Web App hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="95313-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="95313-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95313-110">EXAMPLES</span></span>

### <span data-ttu-id="95313-111">Örnek 1: kaynak grubundan Web uygulaması alma</span><span class="sxs-lookup"><span data-stu-id="95313-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -SlotName "Slot001"
```

<span data-ttu-id="95313-112">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan ContosoSite adlı Web uygulamasını alır.</span><span class="sxs-lookup"><span data-stu-id="95313-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="95313-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95313-113">PARAMETERS</span></span>

### <span data-ttu-id="95313-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="95313-114">-AppServicePlan</span></span>
<span data-ttu-id="95313-115">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="95313-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95313-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="95313-116">-Location</span></span>
<span data-ttu-id="95313-117">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="95313-117">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95313-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="95313-118">-Name</span></span>
<span data-ttu-id="95313-119">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="95313-119">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95313-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95313-120">-ResourceGroupName</span></span>
<span data-ttu-id="95313-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="95313-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95313-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95313-122">-DefaultProfile</span></span>
<span data-ttu-id="95313-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95313-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95313-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95313-124">CommonParameters</span></span>
<span data-ttu-id="95313-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95313-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95313-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95313-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95313-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95313-127">INPUTS</span></span>

## <span data-ttu-id="95313-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95313-128">OUTPUTS</span></span>

## <span data-ttu-id="95313-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95313-129">NOTES</span></span>

## <span data-ttu-id="95313-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95313-130">RELATED LINKS</span></span>

[<span data-ttu-id="95313-131">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="95313-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="95313-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="95313-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="95313-133">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="95313-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="95313-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="95313-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="95313-135">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="95313-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


