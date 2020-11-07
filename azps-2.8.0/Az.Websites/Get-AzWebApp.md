---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: d1217f3abc00fec8752fcddbb30e577df087b5de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917876"
---
# <span data-ttu-id="d51f6-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d51f6-101">Get-AzWebApp</span></span>

## <span data-ttu-id="d51f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d51f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d51f6-103">Belirtilen kaynak grubundaki Azure Web uygulamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="d51f6-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="d51f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d51f6-104">SYNTAX</span></span>

### <span data-ttu-id="d51f6-105">S1</span><span class="sxs-lookup"><span data-stu-id="d51f6-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d51f6-106">S2</span><span class="sxs-lookup"><span data-stu-id="d51f6-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d51f6-107">S3</span><span class="sxs-lookup"><span data-stu-id="d51f6-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d51f6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d51f6-108">DESCRIPTION</span></span>
<span data-ttu-id="d51f6-109">**Get-AzWebApp** cmdlet 'ı bir Azure Web App hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d51f6-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="d51f6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d51f6-110">EXAMPLES</span></span>

### <span data-ttu-id="d51f6-111">Örnek 1: kaynak grubundan Web uygulaması alma</span><span class="sxs-lookup"><span data-stu-id="d51f6-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="d51f6-112">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan ContosoSite adlı Web uygulamasını alır.</span><span class="sxs-lookup"><span data-stu-id="d51f6-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d51f6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d51f6-113">PARAMETERS</span></span>

### <span data-ttu-id="d51f6-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d51f6-114">-AppServicePlan</span></span>
<span data-ttu-id="d51f6-115">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="d51f6-115">App Service Plan object</span></span>

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

### <span data-ttu-id="d51f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d51f6-116">-DefaultProfile</span></span>
<span data-ttu-id="d51f6-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d51f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d51f6-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="d51f6-118">-Location</span></span>
<span data-ttu-id="d51f6-119">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="d51f6-119">Location</span></span>

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

### <span data-ttu-id="d51f6-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="d51f6-120">-Name</span></span>
<span data-ttu-id="d51f6-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="d51f6-121">WebApp Name</span></span>

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

### <span data-ttu-id="d51f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d51f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="d51f6-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d51f6-123">Resource Group Name</span></span>

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

### <span data-ttu-id="d51f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d51f6-124">CommonParameters</span></span>
<span data-ttu-id="d51f6-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d51f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d51f6-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d51f6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d51f6-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d51f6-127">INPUTS</span></span>

### <span data-ttu-id="d51f6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d51f6-128">System.String</span></span>

## <span data-ttu-id="d51f6-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d51f6-129">OUTPUTS</span></span>

### <span data-ttu-id="d51f6-130">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="d51f6-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d51f6-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d51f6-131">NOTES</span></span>

## <span data-ttu-id="d51f6-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d51f6-132">RELATED LINKS</span></span>

[<span data-ttu-id="d51f6-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d51f6-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="d51f6-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d51f6-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="d51f6-135">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d51f6-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="d51f6-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d51f6-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="d51f6-137">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d51f6-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


