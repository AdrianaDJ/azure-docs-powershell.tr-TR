---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 033b0bd4458f20153ec1e9c876f12c7e7c368c0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936103"
---
# <span data-ttu-id="c1e8f-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c1e8f-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="c1e8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="c1e8f-103">Bir Azure Web App yuvası alır.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="c1e8f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1e8f-104">SYNTAX</span></span>

### <span data-ttu-id="c1e8f-105">S1</span><span class="sxs-lookup"><span data-stu-id="c1e8f-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1e8f-106">S2</span><span class="sxs-lookup"><span data-stu-id="c1e8f-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1e8f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1e8f-107">DESCRIPTION</span></span>
<span data-ttu-id="c1e8f-108">**Get-AzWebAppSlot** cmdlet 'ı bir Azure Web App yuvası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="c1e8f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1e8f-109">EXAMPLES</span></span>

### <span data-ttu-id="c1e8f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c1e8f-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="c1e8f-111">Bu komut, Default-Web-WestUS kaynak grubuna ait olan WebAppStandard adlı Web uygulamasından Slot001 adlı yuvayı alır.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c1e8f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1e8f-112">PARAMETERS</span></span>

### <span data-ttu-id="c1e8f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1e8f-113">-DefaultProfile</span></span>
<span data-ttu-id="c1e8f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1e8f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="c1e8f-115">-Name</span></span>
<span data-ttu-id="c1e8f-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="c1e8f-116">WebApp Name</span></span>

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

### <span data-ttu-id="c1e8f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1e8f-117">-ResourceGroupName</span></span>
<span data-ttu-id="c1e8f-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c1e8f-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c1e8f-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="c1e8f-119">-Slot</span></span>
<span data-ttu-id="c1e8f-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="c1e8f-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e8f-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c1e8f-121">-WebApp</span></span>
<span data-ttu-id="c1e8f-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="c1e8f-122">WebApp Object</span></span>

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

### <span data-ttu-id="c1e8f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1e8f-123">CommonParameters</span></span>
<span data-ttu-id="c1e8f-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1e8f-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1e8f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1e8f-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1e8f-126">INPUTS</span></span>

### <span data-ttu-id="c1e8f-127">Bölge</span><span class="sxs-lookup"><span data-stu-id="c1e8f-127">Site</span></span>
<span data-ttu-id="c1e8f-128">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c1e8f-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c1e8f-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1e8f-129">OUTPUTS</span></span>

## <span data-ttu-id="c1e8f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1e8f-130">NOTES</span></span>

## <span data-ttu-id="c1e8f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1e8f-131">RELATED LINKS</span></span>

[<span data-ttu-id="c1e8f-132">Yeni-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c1e8f-132">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="c1e8f-133">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c1e8f-133">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="c1e8f-134">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c1e8f-134">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="c1e8f-135">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c1e8f-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="c1e8f-136">Başlangıç-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c1e8f-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="c1e8f-137">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c1e8f-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="c1e8f-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c1e8f-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
