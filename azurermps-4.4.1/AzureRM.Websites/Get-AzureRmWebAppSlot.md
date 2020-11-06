---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
ms.openlocfilehash: 841cc1f8356d9b082dec55e689033c19343041d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589011"
---
# <span data-ttu-id="d43d8-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d43d8-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="d43d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d43d8-102">SYNOPSIS</span></span>
<span data-ttu-id="d43d8-103">Bir Azure Web App yuvası alır.</span><span class="sxs-lookup"><span data-stu-id="d43d8-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d43d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d43d8-104">SYNTAX</span></span>

### <span data-ttu-id="d43d8-105">S1</span><span class="sxs-lookup"><span data-stu-id="d43d8-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d43d8-106">S2</span><span class="sxs-lookup"><span data-stu-id="d43d8-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d43d8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d43d8-107">DESCRIPTION</span></span>
<span data-ttu-id="d43d8-108">**Get-AzureRmWebAppSlot** cmdlet 'ı Azure Web App yuvası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d43d8-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="d43d8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d43d8-109">EXAMPLES</span></span>

### <span data-ttu-id="d43d8-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d43d8-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="d43d8-111">Bu komut, Default-Web-WestUS kaynak grubuna ait olan WebAppStandard adlı Web uygulamasından Slot001 adlı yuvayı alır.</span><span class="sxs-lookup"><span data-stu-id="d43d8-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d43d8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d43d8-112">PARAMETERS</span></span>

### <span data-ttu-id="d43d8-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="d43d8-113">-Name</span></span>
<span data-ttu-id="d43d8-114">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="d43d8-114">WebApp Name</span></span>

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

### <span data-ttu-id="d43d8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d43d8-115">-ResourceGroupName</span></span>
<span data-ttu-id="d43d8-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d43d8-116">Resource Group Name</span></span>

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

### <span data-ttu-id="d43d8-117">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="d43d8-117">-Slot</span></span>
<span data-ttu-id="d43d8-118">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="d43d8-118">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43d8-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d43d8-119">-WebApp</span></span>
<span data-ttu-id="d43d8-120">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="d43d8-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d43d8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d43d8-121">-DefaultProfile</span></span>
<span data-ttu-id="d43d8-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d43d8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d43d8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d43d8-123">CommonParameters</span></span>
<span data-ttu-id="d43d8-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d43d8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d43d8-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d43d8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d43d8-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d43d8-126">INPUTS</span></span>

### <span data-ttu-id="d43d8-127">Bölge</span><span class="sxs-lookup"><span data-stu-id="d43d8-127">Site</span></span>
<span data-ttu-id="d43d8-128">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d43d8-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d43d8-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d43d8-129">OUTPUTS</span></span>

## <span data-ttu-id="d43d8-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d43d8-130">NOTES</span></span>

## <span data-ttu-id="d43d8-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d43d8-131">RELATED LINKS</span></span>

[<span data-ttu-id="d43d8-132">Yeni-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d43d8-132">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="d43d8-133">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d43d8-133">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="d43d8-134">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d43d8-134">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="d43d8-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d43d8-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="d43d8-136">Başlangıç-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d43d8-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="d43d8-137">Dur-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d43d8-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="d43d8-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="d43d8-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
