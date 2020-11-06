---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmFirewall.md
ms.openlocfilehash: 1a6c5ae69ef6aa6dc0f64d118fcbc733c97e23a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589440"
---
# <span data-ttu-id="38fed-101">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="38fed-101">Remove-AzureRmFirewall</span></span>

## <span data-ttu-id="38fed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38fed-102">SYNOPSIS</span></span>
<span data-ttu-id="38fed-103">Güvenlik duvarını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="38fed-103">Remove a Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38fed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38fed-104">SYNTAX</span></span>

```
Remove-AzureRmFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38fed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="38fed-105">DESCRIPTION</span></span>
<span data-ttu-id="38fed-106">**Remove-AzureRmFirewall** cmdlet 'ı bir Azure Güvenlik duvarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="38fed-106">The **Remove-AzureRmFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="38fed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38fed-107">EXAMPLES</span></span>

### <span data-ttu-id="38fed-108">1: güvenlik duvarı oluşturma ve silme</span><span class="sxs-lookup"><span data-stu-id="38fed-108">1: Create and delete a Firewall</span></span>
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="38fed-109">Bu örnekte bir güvenlik duvarı oluşturulur ve sonra silinir.</span><span class="sxs-lookup"><span data-stu-id="38fed-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="38fed-110">Güvenlik duvarını silerken komut istemini bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="38fed-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

### <span data-ttu-id="38fed-111">2: güvenlik duvarını serbest bırakma ve güvenlik duvarını silme</span><span class="sxs-lookup"><span data-stu-id="38fed-111">2: Deallocate the Firewall, then delete the Firewall</span></span>
```
$firewall=Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
Remove-AzureRmFirewall -ResourceGroupName rgName -Name azFw
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="38fed-112">Bu örnekte bir güvenlik duvarı alınır, güvenlik duvarını ayırır ve güvenlik duvarı silinir.</span><span class="sxs-lookup"><span data-stu-id="38fed-112">This example retrieves a Firewall, deallocates the firewall, and then deletes the firewall.</span></span> <span data-ttu-id="38fed-113">Serbest bırakma komutu, çalışan hizmeti kaldırır ancak güvenlik duvarının yapılandırmasını korur.</span><span class="sxs-lookup"><span data-stu-id="38fed-113">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="38fed-114">Kullanıcı Hizmeti yeniden başlatmak istiyorsa, ayırma yöntemi güvenlik duvarında çağrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="38fed-114">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="38fed-115">Güvenlik duvarını silerken komut istemini bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="38fed-115">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="38fed-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38fed-116">PARAMETERS</span></span>

### <span data-ttu-id="38fed-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="38fed-117">-AsJob</span></span>
<span data-ttu-id="38fed-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="38fed-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38fed-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38fed-119">-DefaultProfile</span></span>
<span data-ttu-id="38fed-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38fed-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38fed-121">-Force</span><span class="sxs-lookup"><span data-stu-id="38fed-121">-Force</span></span>
<span data-ttu-id="38fed-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="38fed-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="38fed-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="38fed-123">-Name</span></span>
<span data-ttu-id="38fed-124">Bu cmdlet 'in kaldırdığı güvenlik duvarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38fed-124">Specifies the name of the firewall that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38fed-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="38fed-125">-PassThru</span></span>
<span data-ttu-id="38fed-126">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="38fed-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="38fed-127">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="38fed-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="38fed-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38fed-128">-ResourceGroupName</span></span>
<span data-ttu-id="38fed-129">Bu cmdlet 'in kaldırdığı güvenlik duvarını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38fed-129">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38fed-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="38fed-130">-Confirm</span></span>
<span data-ttu-id="38fed-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="38fed-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38fed-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38fed-132">-WhatIf</span></span>
<span data-ttu-id="38fed-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="38fed-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38fed-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="38fed-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38fed-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38fed-135">CommonParameters</span></span>
<span data-ttu-id="38fed-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38fed-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38fed-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38fed-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38fed-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38fed-138">INPUTS</span></span>

### <span data-ttu-id="38fed-139">PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="38fed-139">PSAzureFirewall</span></span>
<span data-ttu-id="38fed-140">Ardışık düzen için ' PSAzureFirewall ' türü kabul edildi</span><span class="sxs-lookup"><span data-stu-id="38fed-140">Type 'PSAzureFirewall' is accepted from the pipeline</span></span>

## <span data-ttu-id="38fed-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38fed-141">OUTPUTS</span></span>

## <span data-ttu-id="38fed-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38fed-142">NOTES</span></span>

## <span data-ttu-id="38fed-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38fed-143">RELATED LINKS</span></span>

[<span data-ttu-id="38fed-144">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="38fed-144">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="38fed-145">Yeni-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="38fed-145">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="38fed-146">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="38fed-146">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)
