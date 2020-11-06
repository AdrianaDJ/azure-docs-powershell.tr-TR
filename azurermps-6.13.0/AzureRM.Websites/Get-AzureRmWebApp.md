---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 83afdb179a9c0f135fd17827ff59f89ad117e3b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590790"
---
# <span data-ttu-id="478ea-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="478ea-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="478ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="478ea-102">SYNOPSIS</span></span>
<span data-ttu-id="478ea-103">Belirtilen kaynak grubundaki Azure Web uygulamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="478ea-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="478ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="478ea-104">SYNTAX</span></span>

### <span data-ttu-id="478ea-105">S1</span><span class="sxs-lookup"><span data-stu-id="478ea-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="478ea-106">S2</span><span class="sxs-lookup"><span data-stu-id="478ea-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="478ea-107">S3</span><span class="sxs-lookup"><span data-stu-id="478ea-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="478ea-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="478ea-108">DESCRIPTION</span></span>
<span data-ttu-id="478ea-109">**Get-AzureRmWebApp** cmdlet 'ı bir Azure Web App hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="478ea-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="478ea-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="478ea-110">EXAMPLES</span></span>

### <span data-ttu-id="478ea-111">Örnek 1: kaynak grubundan Web uygulaması alma</span><span class="sxs-lookup"><span data-stu-id="478ea-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="478ea-112">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan ContosoSite adlı Web uygulamasını alır.</span><span class="sxs-lookup"><span data-stu-id="478ea-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="478ea-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="478ea-113">PARAMETERS</span></span>

### <span data-ttu-id="478ea-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="478ea-114">-AppServicePlan</span></span>
<span data-ttu-id="478ea-115">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="478ea-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="478ea-116">-DefaultProfile</span></span>
<span data-ttu-id="478ea-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="478ea-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="478ea-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="478ea-118">-Location</span></span>
<span data-ttu-id="478ea-119">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="478ea-119">Location</span></span>

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

### <span data-ttu-id="478ea-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="478ea-120">-Name</span></span>
<span data-ttu-id="478ea-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="478ea-121">WebApp Name</span></span>

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

### <span data-ttu-id="478ea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="478ea-122">-ResourceGroupName</span></span>
<span data-ttu-id="478ea-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="478ea-123">Resource Group Name</span></span>

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

### <span data-ttu-id="478ea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="478ea-124">CommonParameters</span></span>
<span data-ttu-id="478ea-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="478ea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="478ea-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="478ea-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="478ea-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="478ea-127">INPUTS</span></span>

### <span data-ttu-id="478ea-128">System. String</span><span class="sxs-lookup"><span data-stu-id="478ea-128">System.String</span></span>

## <span data-ttu-id="478ea-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="478ea-129">OUTPUTS</span></span>

### <span data-ttu-id="478ea-130">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="478ea-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="478ea-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="478ea-131">NOTES</span></span>

## <span data-ttu-id="478ea-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="478ea-132">RELATED LINKS</span></span>

[<span data-ttu-id="478ea-133">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="478ea-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="478ea-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="478ea-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="478ea-135">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="478ea-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="478ea-136">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="478ea-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="478ea-137">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="478ea-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


