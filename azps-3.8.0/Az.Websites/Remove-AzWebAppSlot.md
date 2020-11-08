---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 88eaf66ea8584913c7816fd12be19509aec49de5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098397"
---
# <span data-ttu-id="37828-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="37828-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="37828-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37828-102">SYNOPSIS</span></span>

## <span data-ttu-id="37828-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37828-103">SYNTAX</span></span>

### <span data-ttu-id="37828-104">S1</span><span class="sxs-lookup"><span data-stu-id="37828-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37828-105">S2</span><span class="sxs-lookup"><span data-stu-id="37828-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37828-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="37828-106">DESCRIPTION</span></span>
<span data-ttu-id="37828-107">**Remove-AzWebAppSlot** cmdlet 'i, kaynak grubuna ve Web uygulaması adına sağlanan bir Azure Web App yuvasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="37828-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="37828-108">Bu cmdlet varsayılan olarak tüm yuvaları ve ölçümleri de kaldırır.</span><span class="sxs-lookup"><span data-stu-id="37828-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="37828-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37828-109">EXAMPLES</span></span>

### <span data-ttu-id="37828-110">Örnek 1: Web uygulaması yuvasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="37828-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="37828-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait Web App Contosositesiyle ilişkili Slot001 adlı yuvayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="37828-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="37828-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37828-112">PARAMETERS</span></span>

### <span data-ttu-id="37828-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="37828-113">-AsJob</span></span>
<span data-ttu-id="37828-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="37828-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37828-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37828-115">-DefaultProfile</span></span>
<span data-ttu-id="37828-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="37828-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37828-117">-Force</span><span class="sxs-lookup"><span data-stu-id="37828-117">-Force</span></span>
<span data-ttu-id="37828-118">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="37828-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="37828-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="37828-119">-Name</span></span>
<span data-ttu-id="37828-120">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="37828-120">WebApp Name</span></span>

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

### <span data-ttu-id="37828-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37828-121">-ResourceGroupName</span></span>
<span data-ttu-id="37828-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="37828-122">Resource Group Name</span></span>

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

### <span data-ttu-id="37828-123">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="37828-123">-Slot</span></span>
<span data-ttu-id="37828-124">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="37828-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="37828-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="37828-125">-WebApp</span></span>
<span data-ttu-id="37828-126">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="37828-126">WebApp Object</span></span>

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

### <span data-ttu-id="37828-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="37828-127">-Confirm</span></span>
<span data-ttu-id="37828-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="37828-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37828-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37828-129">-WhatIf</span></span>
<span data-ttu-id="37828-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="37828-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37828-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="37828-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37828-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37828-132">CommonParameters</span></span>
<span data-ttu-id="37828-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37828-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37828-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37828-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37828-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37828-135">INPUTS</span></span>

### <span data-ttu-id="37828-136">System. String</span><span class="sxs-lookup"><span data-stu-id="37828-136">System.String</span></span>

### <span data-ttu-id="37828-137">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="37828-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="37828-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37828-138">OUTPUTS</span></span>

### <span data-ttu-id="37828-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="37828-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="37828-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37828-140">NOTES</span></span>

## <span data-ttu-id="37828-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37828-141">RELATED LINKS</span></span>

[<span data-ttu-id="37828-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="37828-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="37828-143">Yeni-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="37828-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="37828-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="37828-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="37828-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="37828-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="37828-146">Başlangıç-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="37828-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="37828-147">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="37828-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="37828-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="37828-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)