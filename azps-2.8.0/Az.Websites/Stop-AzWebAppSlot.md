---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: 455a1735df128ee84d99adb6461c602a7b1dbbdf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933908"
---
# <span data-ttu-id="aa432-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="aa432-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="aa432-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa432-102">SYNOPSIS</span></span>
<span data-ttu-id="aa432-103">Azure Web App yuvasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="aa432-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="aa432-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa432-104">SYNTAX</span></span>

### <span data-ttu-id="aa432-105">S1</span><span class="sxs-lookup"><span data-stu-id="aa432-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa432-106">S2</span><span class="sxs-lookup"><span data-stu-id="aa432-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa432-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa432-107">DESCRIPTION</span></span>
<span data-ttu-id="aa432-108">**Stop-AzWebAppSlot** cmdlet 'ı bir Azure Web App yuvasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="aa432-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="aa432-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa432-109">EXAMPLES</span></span>

### <span data-ttu-id="aa432-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aa432-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="aa432-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoWebApp adlı Web uygulamasının bulunduğu yuva Slot001.</span><span class="sxs-lookup"><span data-stu-id="aa432-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="aa432-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa432-112">PARAMETERS</span></span>

### <span data-ttu-id="aa432-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa432-113">-DefaultProfile</span></span>
<span data-ttu-id="aa432-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aa432-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa432-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="aa432-115">-Name</span></span>
<span data-ttu-id="aa432-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="aa432-116">WebApp Name</span></span>

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

### <span data-ttu-id="aa432-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa432-117">-ResourceGroupName</span></span>
<span data-ttu-id="aa432-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="aa432-118">Resource Group Name</span></span>

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

### <span data-ttu-id="aa432-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="aa432-119">-Slot</span></span>
<span data-ttu-id="aa432-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="aa432-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="aa432-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="aa432-121">-WebApp</span></span>
<span data-ttu-id="aa432-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="aa432-122">WebApp Object</span></span>

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

### <span data-ttu-id="aa432-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa432-123">CommonParameters</span></span>
<span data-ttu-id="aa432-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa432-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa432-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa432-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa432-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa432-126">INPUTS</span></span>

### <span data-ttu-id="aa432-127">System. String</span><span class="sxs-lookup"><span data-stu-id="aa432-127">System.String</span></span>

### <span data-ttu-id="aa432-128">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="aa432-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="aa432-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa432-129">OUTPUTS</span></span>

### <span data-ttu-id="aa432-130">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="aa432-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="aa432-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa432-131">NOTES</span></span>

## <span data-ttu-id="aa432-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa432-132">RELATED LINKS</span></span>