---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 93db0a86caf381b32293089bd68a6efafc20ef02
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939827"
---
# <span data-ttu-id="500c2-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="500c2-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="500c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="500c2-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="500c2-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="500c2-103">SYNTAX</span></span>

### <span data-ttu-id="500c2-104">S1</span><span class="sxs-lookup"><span data-stu-id="500c2-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="500c2-105">S2</span><span class="sxs-lookup"><span data-stu-id="500c2-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="500c2-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="500c2-106">DESCRIPTION</span></span>
<span data-ttu-id="500c2-107">**Remove-AzureRmWebAppSlot** cmdlet 'i, kaynak grubuna ve Web uygulaması adına sağlanan bir Azure Web App yuvasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="500c2-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="500c2-108">Bu cmdlet varsayılan olarak tüm yuvaları ve ölçümleri de kaldırır.</span><span class="sxs-lookup"><span data-stu-id="500c2-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="500c2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="500c2-109">EXAMPLES</span></span>

### <span data-ttu-id="500c2-110">Örnek 1: Web uygulaması yuvasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="500c2-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="500c2-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait Web App Contosositesiyle ilişkili Slot001 adlı yuvayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="500c2-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="500c2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="500c2-112">PARAMETERS</span></span>

### <span data-ttu-id="500c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500c2-113">-DefaultProfile</span></span>
<span data-ttu-id="500c2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="500c2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500c2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="500c2-115">-Force</span></span>
<span data-ttu-id="500c2-116">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="500c2-116">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500c2-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="500c2-117">-Name</span></span>
<span data-ttu-id="500c2-118">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="500c2-118">WebApp Name</span></span>

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

### <span data-ttu-id="500c2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="500c2-119">-ResourceGroupName</span></span>
<span data-ttu-id="500c2-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="500c2-120">Resource Group Name</span></span>

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

### <span data-ttu-id="500c2-121">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="500c2-121">-Slot</span></span>
<span data-ttu-id="500c2-122">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="500c2-122">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500c2-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="500c2-123">-WebApp</span></span>
<span data-ttu-id="500c2-124">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="500c2-124">WebApp Object</span></span>

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

### <span data-ttu-id="500c2-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="500c2-125">-Confirm</span></span>
<span data-ttu-id="500c2-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="500c2-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500c2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="500c2-127">-WhatIf</span></span>
<span data-ttu-id="500c2-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="500c2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="500c2-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="500c2-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="500c2-130">-Iş</span><span class="sxs-lookup"><span data-stu-id="500c2-130">-AsJob</span></span>
<span data-ttu-id="500c2-131">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="500c2-131">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500c2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500c2-132">CommonParameters</span></span>
<span data-ttu-id="500c2-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="500c2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500c2-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="500c2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500c2-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="500c2-135">INPUTS</span></span>

### <span data-ttu-id="500c2-136">Bölge</span><span class="sxs-lookup"><span data-stu-id="500c2-136">Site</span></span>
<span data-ttu-id="500c2-137">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="500c2-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="500c2-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="500c2-138">OUTPUTS</span></span>

### <span data-ttu-id="500c2-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="500c2-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="500c2-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="500c2-140">NOTES</span></span>

## <span data-ttu-id="500c2-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="500c2-141">RELATED LINKS</span></span>

[<span data-ttu-id="500c2-142">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="500c2-142">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="500c2-143">Yeni-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="500c2-143">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="500c2-144">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="500c2-144">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="500c2-145">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="500c2-145">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="500c2-146">Başlangıç-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="500c2-146">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="500c2-147">Dur-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="500c2-147">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="500c2-148">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="500c2-148">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)