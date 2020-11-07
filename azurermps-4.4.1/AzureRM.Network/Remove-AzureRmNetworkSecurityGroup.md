---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: fd6d9a09bd2c4fa597d2c384d3ba8e730b3f1102
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762563"
---
# <span data-ttu-id="578a6-101">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="578a6-101">Remove-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="578a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="578a6-102">SYNOPSIS</span></span>
<span data-ttu-id="578a6-103">Ağ güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="578a6-103">Removes a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="578a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="578a6-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="578a6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="578a6-105">DESCRIPTION</span></span>
<span data-ttu-id="578a6-106">**Remove-AzureRmNetworkSecurityGroup** cmdlet 'ı bir Azure ağ güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="578a6-106">The **Remove-AzureRmNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="578a6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="578a6-107">EXAMPLES</span></span>

### <span data-ttu-id="578a6-108">Örnek 1: ağ güvenlik grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="578a6-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="578a6-109">Bu komut, TestRG adlı kaynak grubundaki NSG-FrontEnd adındaki güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="578a6-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="578a6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="578a6-110">PARAMETERS</span></span>

### <span data-ttu-id="578a6-111">-Force</span><span class="sxs-lookup"><span data-stu-id="578a6-111">-Force</span></span>
<span data-ttu-id="578a6-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="578a6-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="578a6-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="578a6-113">-Name</span></span>
<span data-ttu-id="578a6-114">Bu cmdlet 'in kaldırdığı ağ güvenlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="578a6-114">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="578a6-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="578a6-115">-PassThru</span></span>
<span data-ttu-id="578a6-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="578a6-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="578a6-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="578a6-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="578a6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="578a6-118">-ResourceGroupName</span></span>
<span data-ttu-id="578a6-119">Bu cmdlet 'in uygulamasından ağ güvenlik grubunu kaldıran bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="578a6-119">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="578a6-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="578a6-120">-Confirm</span></span>
<span data-ttu-id="578a6-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="578a6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="578a6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="578a6-122">-WhatIf</span></span>
<span data-ttu-id="578a6-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="578a6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="578a6-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="578a6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="578a6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="578a6-125">-DefaultProfile</span></span>
<span data-ttu-id="578a6-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="578a6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="578a6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="578a6-127">CommonParameters</span></span>
<span data-ttu-id="578a6-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="578a6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="578a6-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="578a6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="578a6-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="578a6-130">INPUTS</span></span>

## <span data-ttu-id="578a6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="578a6-131">OUTPUTS</span></span>

## <span data-ttu-id="578a6-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="578a6-132">NOTES</span></span>

## <span data-ttu-id="578a6-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="578a6-133">RELATED LINKS</span></span>

[<span data-ttu-id="578a6-134">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="578a6-134">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="578a6-135">Yeni-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="578a6-135">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="578a6-136">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="578a6-136">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


