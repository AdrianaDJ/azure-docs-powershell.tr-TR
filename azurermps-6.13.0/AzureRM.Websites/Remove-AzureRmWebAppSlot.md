---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 7fdf5e8de2ec326888c57e8219a006f9ef447aa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590788"
---
# <span data-ttu-id="dd8ec-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dd8ec-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="dd8ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd8ec-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd8ec-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd8ec-103">SYNTAX</span></span>

### <span data-ttu-id="dd8ec-104">S1</span><span class="sxs-lookup"><span data-stu-id="dd8ec-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd8ec-105">S2</span><span class="sxs-lookup"><span data-stu-id="dd8ec-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd8ec-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd8ec-106">DESCRIPTION</span></span>
<span data-ttu-id="dd8ec-107">**Remove-AzureRmWebAppSlot** cmdlet 'i, kaynak grubuna ve Web uygulaması adına sağlanan bir Azure Web App yuvasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dd8ec-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="dd8ec-108">Bu cmdlet varsayılan olarak tüm yuvaları ve ölçümleri de kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dd8ec-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="dd8ec-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd8ec-109">EXAMPLES</span></span>

### <span data-ttu-id="dd8ec-110">Örnek 1: Web uygulaması yuvasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="dd8ec-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="dd8ec-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait Web App Contosositesiyle ilişkili Slot001 adlı yuvayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dd8ec-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="dd8ec-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd8ec-112">PARAMETERS</span></span>

### <span data-ttu-id="dd8ec-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="dd8ec-113">-AsJob</span></span>
<span data-ttu-id="dd8ec-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="dd8ec-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd8ec-115">-DefaultProfile</span></span>
<span data-ttu-id="dd8ec-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd8ec-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd8ec-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dd8ec-117">-Force</span></span>
<span data-ttu-id="dd8ec-118">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="dd8ec-118">Forcefully Remove Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8ec-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd8ec-119">-Name</span></span>
<span data-ttu-id="dd8ec-120">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="dd8ec-120">WebApp Name</span></span>

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

### <span data-ttu-id="dd8ec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd8ec-121">-ResourceGroupName</span></span>
<span data-ttu-id="dd8ec-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="dd8ec-122">Resource Group Name</span></span>

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

### <span data-ttu-id="dd8ec-123">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="dd8ec-123">-Slot</span></span>
<span data-ttu-id="dd8ec-124">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="dd8ec-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="dd8ec-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="dd8ec-125">-WebApp</span></span>
<span data-ttu-id="dd8ec-126">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="dd8ec-126">WebApp Object</span></span>

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

### <span data-ttu-id="dd8ec-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="dd8ec-127">-Confirm</span></span>
<span data-ttu-id="dd8ec-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dd8ec-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8ec-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd8ec-129">-WhatIf</span></span>
<span data-ttu-id="dd8ec-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd8ec-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd8ec-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dd8ec-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8ec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8ec-132">CommonParameters</span></span>
<span data-ttu-id="dd8ec-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd8ec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd8ec-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd8ec-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8ec-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd8ec-135">INPUTS</span></span>

### <span data-ttu-id="dd8ec-136">System. String</span><span class="sxs-lookup"><span data-stu-id="dd8ec-136">System.String</span></span>

### <span data-ttu-id="dd8ec-137">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="dd8ec-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="dd8ec-138">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dd8ec-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="dd8ec-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd8ec-139">OUTPUTS</span></span>

### <span data-ttu-id="dd8ec-140">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="dd8ec-140">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="dd8ec-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd8ec-141">NOTES</span></span>

## <span data-ttu-id="dd8ec-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd8ec-142">RELATED LINKS</span></span>

[<span data-ttu-id="dd8ec-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dd8ec-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="dd8ec-144">Yeni-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dd8ec-144">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="dd8ec-145">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dd8ec-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="dd8ec-146">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dd8ec-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="dd8ec-147">Başlangıç-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dd8ec-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="dd8ec-148">Dur-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dd8ec-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="dd8ec-149">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="dd8ec-149">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
