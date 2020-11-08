---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097489"
---
# <span data-ttu-id="64d35-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="64d35-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="64d35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64d35-102">SYNOPSIS</span></span>
<span data-ttu-id="64d35-103">Bir Azure Web App yuvası alır.</span><span class="sxs-lookup"><span data-stu-id="64d35-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="64d35-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64d35-104">SYNTAX</span></span>

### <span data-ttu-id="64d35-105">S1</span><span class="sxs-lookup"><span data-stu-id="64d35-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64d35-106">S2</span><span class="sxs-lookup"><span data-stu-id="64d35-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64d35-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="64d35-107">DESCRIPTION</span></span>
<span data-ttu-id="64d35-108">**Get-AzWebAppSlot** cmdlet 'ı bir Azure Web App yuvası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="64d35-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="64d35-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64d35-109">EXAMPLES</span></span>

### <span data-ttu-id="64d35-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="64d35-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="64d35-111">Bu komut, Default-Web-WestUS kaynak grubuna ait olan WebAppStandard adlı Web uygulamasından Slot001 adlı yuvayı alır.</span><span class="sxs-lookup"><span data-stu-id="64d35-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="64d35-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64d35-112">PARAMETERS</span></span>

### <span data-ttu-id="64d35-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d35-113">-DefaultProfile</span></span>
<span data-ttu-id="64d35-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="64d35-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64d35-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="64d35-115">-Name</span></span>
<span data-ttu-id="64d35-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="64d35-116">WebApp Name</span></span>

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

### <span data-ttu-id="64d35-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64d35-117">-ResourceGroupName</span></span>
<span data-ttu-id="64d35-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="64d35-118">Resource Group Name</span></span>

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

### <span data-ttu-id="64d35-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="64d35-119">-Slot</span></span>
<span data-ttu-id="64d35-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="64d35-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="64d35-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="64d35-121">-WebApp</span></span>
<span data-ttu-id="64d35-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="64d35-122">WebApp Object</span></span>

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

### <span data-ttu-id="64d35-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d35-123">CommonParameters</span></span>
<span data-ttu-id="64d35-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64d35-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d35-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64d35-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d35-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64d35-126">INPUTS</span></span>

### <span data-ttu-id="64d35-127">System. String</span><span class="sxs-lookup"><span data-stu-id="64d35-127">System.String</span></span>

### <span data-ttu-id="64d35-128">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="64d35-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="64d35-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64d35-129">OUTPUTS</span></span>

### <span data-ttu-id="64d35-130">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="64d35-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="64d35-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64d35-131">NOTES</span></span>

## <span data-ttu-id="64d35-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64d35-132">RELATED LINKS</span></span>

[<span data-ttu-id="64d35-133">Yeni-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="64d35-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="64d35-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="64d35-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="64d35-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="64d35-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="64d35-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="64d35-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="64d35-137">Başlangıç-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="64d35-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="64d35-138">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="64d35-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="64d35-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="64d35-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
