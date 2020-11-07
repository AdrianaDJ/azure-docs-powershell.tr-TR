---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 4fb9c12f1c3fe79eb09a1f98d4f6b484d93556b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593965"
---
# <span data-ttu-id="0e13f-101">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0e13f-101">Remove-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="0e13f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e13f-102">SYNOPSIS</span></span>
<span data-ttu-id="0e13f-103">Ağ güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0e13f-103">Removes a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e13f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e13f-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e13f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e13f-105">DESCRIPTION</span></span>
<span data-ttu-id="0e13f-106">**Remove-AzureRmNetworkSecurityGroup** cmdlet 'ı bir Azure ağ güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0e13f-106">The **Remove-AzureRmNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="0e13f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e13f-107">EXAMPLES</span></span>

### <span data-ttu-id="0e13f-108">Örnek 1: ağ güvenlik grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="0e13f-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="0e13f-109">Bu komut, TestRG adlı kaynak grubundaki NSG-FrontEnd adındaki güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0e13f-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="0e13f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e13f-110">PARAMETERS</span></span>

### <span data-ttu-id="0e13f-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="0e13f-111">-AsJob</span></span>
<span data-ttu-id="0e13f-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0e13f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e13f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e13f-113">-DefaultProfile</span></span>
<span data-ttu-id="0e13f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0e13f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e13f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0e13f-115">-Force</span></span>
<span data-ttu-id="0e13f-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="0e13f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0e13f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="0e13f-117">-Name</span></span>
<span data-ttu-id="0e13f-118">Bu cmdlet 'in kaldırdığı ağ güvenlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e13f-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e13f-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0e13f-119">-PassThru</span></span>
<span data-ttu-id="0e13f-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="0e13f-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0e13f-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0e13f-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0e13f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e13f-122">-ResourceGroupName</span></span>
<span data-ttu-id="0e13f-123">Bu cmdlet 'in uygulamasından ağ güvenlik grubunu kaldıran bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e13f-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e13f-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="0e13f-124">-Confirm</span></span>
<span data-ttu-id="0e13f-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0e13f-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e13f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e13f-126">-WhatIf</span></span>
<span data-ttu-id="0e13f-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0e13f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e13f-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0e13f-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e13f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e13f-129">CommonParameters</span></span>
<span data-ttu-id="0e13f-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e13f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e13f-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e13f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e13f-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e13f-132">INPUTS</span></span>

### <span data-ttu-id="0e13f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0e13f-133">System.String</span></span>

## <span data-ttu-id="0e13f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e13f-134">OUTPUTS</span></span>

### <span data-ttu-id="0e13f-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e13f-135">System.Boolean</span></span>

## <span data-ttu-id="0e13f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e13f-136">NOTES</span></span>

## <span data-ttu-id="0e13f-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e13f-137">RELATED LINKS</span></span>

[<span data-ttu-id="0e13f-138">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0e13f-138">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="0e13f-139">Yeni-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0e13f-139">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="0e13f-140">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0e13f-140">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)

