---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 4425c344fb0c9e0e3441c172915be11002ee8b1b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098065"
---
# <span data-ttu-id="bbb2c-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bbb2c-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="bbb2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbb2c-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb2c-103">Azure Web App yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="bbb2c-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="bbb2c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bbb2c-104">SYNTAX</span></span>

### <span data-ttu-id="bbb2c-105">S1</span><span class="sxs-lookup"><span data-stu-id="bbb2c-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbb2c-106">S2</span><span class="sxs-lookup"><span data-stu-id="bbb2c-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbb2c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bbb2c-107">DESCRIPTION</span></span>
<span data-ttu-id="bbb2c-108">**Start-AzWebAppSlot** cmdlet 'ı Azure Web App yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="bbb2c-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="bbb2c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bbb2c-109">EXAMPLES</span></span>

### <span data-ttu-id="bbb2c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bbb2c-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="bbb2c-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoWebApp adındaki Web uygulamasının Slot001 adlı yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="bbb2c-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="bbb2c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bbb2c-112">PARAMETERS</span></span>

### <span data-ttu-id="bbb2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbb2c-113">-DefaultProfile</span></span>
<span data-ttu-id="bbb2c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bbb2c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbb2c-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="bbb2c-115">-Name</span></span>
<span data-ttu-id="bbb2c-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="bbb2c-116">WebApp Name</span></span>

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

### <span data-ttu-id="bbb2c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbb2c-117">-ResourceGroupName</span></span>
<span data-ttu-id="bbb2c-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="bbb2c-118">Resource Group Name</span></span>

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

### <span data-ttu-id="bbb2c-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="bbb2c-119">-Slot</span></span>
<span data-ttu-id="bbb2c-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="bbb2c-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbb2c-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bbb2c-121">-WebApp</span></span>
<span data-ttu-id="bbb2c-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="bbb2c-122">WebApp Object</span></span>

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

### <span data-ttu-id="bbb2c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb2c-123">CommonParameters</span></span>
<span data-ttu-id="bbb2c-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bbb2c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb2c-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbb2c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb2c-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bbb2c-126">INPUTS</span></span>

### <span data-ttu-id="bbb2c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="bbb2c-127">System.String</span></span>

### <span data-ttu-id="bbb2c-128">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="bbb2c-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="bbb2c-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bbb2c-129">OUTPUTS</span></span>

### <span data-ttu-id="bbb2c-130">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="bbb2c-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="bbb2c-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bbb2c-131">NOTES</span></span>

## <span data-ttu-id="bbb2c-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bbb2c-132">RELATED LINKS</span></span>

[<span data-ttu-id="bbb2c-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bbb2c-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="bbb2c-134">Yeni-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bbb2c-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="bbb2c-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bbb2c-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="bbb2c-136">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bbb2c-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="bbb2c-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bbb2c-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="bbb2c-138">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bbb2c-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="bbb2c-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bbb2c-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
