---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274654"
---
# <span data-ttu-id="44eac-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44eac-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="44eac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44eac-102">SYNOPSIS</span></span>
<span data-ttu-id="44eac-103">Bir Azure Web App yuvası alır.</span><span class="sxs-lookup"><span data-stu-id="44eac-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="44eac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44eac-104">SYNTAX</span></span>

### <span data-ttu-id="44eac-105">S1</span><span class="sxs-lookup"><span data-stu-id="44eac-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44eac-106">S2</span><span class="sxs-lookup"><span data-stu-id="44eac-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44eac-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="44eac-107">DESCRIPTION</span></span>
<span data-ttu-id="44eac-108">**Get-AzWebAppSlot** cmdlet 'ı bir Azure Web App yuvası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="44eac-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="44eac-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44eac-109">EXAMPLES</span></span>

### <span data-ttu-id="44eac-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="44eac-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="44eac-111">Bu komut, Default-Web-WestUS kaynak grubuna ait olan WebAppStandard adlı Web uygulamasından Slot001 adlı yuvayı alır.</span><span class="sxs-lookup"><span data-stu-id="44eac-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="44eac-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44eac-112">PARAMETERS</span></span>

### <span data-ttu-id="44eac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44eac-113">-DefaultProfile</span></span>
<span data-ttu-id="44eac-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="44eac-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44eac-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="44eac-115">-Name</span></span>
<span data-ttu-id="44eac-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="44eac-116">WebApp Name</span></span>

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

### <span data-ttu-id="44eac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44eac-117">-ResourceGroupName</span></span>
<span data-ttu-id="44eac-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="44eac-118">Resource Group Name</span></span>

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

### <span data-ttu-id="44eac-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="44eac-119">-Slot</span></span>
<span data-ttu-id="44eac-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="44eac-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="44eac-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="44eac-121">-WebApp</span></span>
<span data-ttu-id="44eac-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="44eac-122">WebApp Object</span></span>

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

### <span data-ttu-id="44eac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44eac-123">CommonParameters</span></span>
<span data-ttu-id="44eac-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44eac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44eac-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44eac-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44eac-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44eac-126">INPUTS</span></span>

### <span data-ttu-id="44eac-127">System. String</span><span class="sxs-lookup"><span data-stu-id="44eac-127">System.String</span></span>

### <span data-ttu-id="44eac-128">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="44eac-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="44eac-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44eac-129">OUTPUTS</span></span>

### <span data-ttu-id="44eac-130">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="44eac-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="44eac-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44eac-131">NOTES</span></span>

## <span data-ttu-id="44eac-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44eac-132">RELATED LINKS</span></span>

[<span data-ttu-id="44eac-133">Yeni-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44eac-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="44eac-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44eac-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="44eac-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44eac-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="44eac-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44eac-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="44eac-137">Başlangıç-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44eac-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="44eac-138">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44eac-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="44eac-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44eac-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
