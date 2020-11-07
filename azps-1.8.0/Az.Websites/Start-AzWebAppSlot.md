---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 0535eee5dcdc3d0e78f95951fddcca9d7b8fff3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753764"
---
# <span data-ttu-id="63308-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63308-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="63308-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63308-102">SYNOPSIS</span></span>
<span data-ttu-id="63308-103">Azure Web App yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="63308-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="63308-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63308-104">SYNTAX</span></span>

### <span data-ttu-id="63308-105">S1</span><span class="sxs-lookup"><span data-stu-id="63308-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63308-106">S2</span><span class="sxs-lookup"><span data-stu-id="63308-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63308-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="63308-107">DESCRIPTION</span></span>
<span data-ttu-id="63308-108">**Start-AzWebAppSlot** cmdlet 'ı Azure Web App yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="63308-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="63308-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63308-109">EXAMPLES</span></span>

### <span data-ttu-id="63308-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="63308-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="63308-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoWebApp adındaki Web uygulamasının Slot001 adlı yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="63308-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="63308-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63308-112">PARAMETERS</span></span>

### <span data-ttu-id="63308-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63308-113">-DefaultProfile</span></span>
<span data-ttu-id="63308-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="63308-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63308-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="63308-115">-Name</span></span>
<span data-ttu-id="63308-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="63308-116">WebApp Name</span></span>

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

### <span data-ttu-id="63308-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63308-117">-ResourceGroupName</span></span>
<span data-ttu-id="63308-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="63308-118">Resource Group Name</span></span>

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

### <span data-ttu-id="63308-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="63308-119">-Slot</span></span>
<span data-ttu-id="63308-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="63308-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="63308-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="63308-121">-WebApp</span></span>
<span data-ttu-id="63308-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="63308-122">WebApp Object</span></span>

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

### <span data-ttu-id="63308-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63308-123">CommonParameters</span></span>
<span data-ttu-id="63308-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63308-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63308-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63308-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63308-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63308-126">INPUTS</span></span>

### <span data-ttu-id="63308-127">System. String</span><span class="sxs-lookup"><span data-stu-id="63308-127">System.String</span></span>

### <span data-ttu-id="63308-128">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="63308-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="63308-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63308-129">OUTPUTS</span></span>

### <span data-ttu-id="63308-130">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="63308-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="63308-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63308-131">NOTES</span></span>

## <span data-ttu-id="63308-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63308-132">RELATED LINKS</span></span>

[<span data-ttu-id="63308-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63308-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="63308-134">Yeni-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63308-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="63308-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63308-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="63308-136">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63308-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="63308-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63308-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="63308-138">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63308-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="63308-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="63308-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
