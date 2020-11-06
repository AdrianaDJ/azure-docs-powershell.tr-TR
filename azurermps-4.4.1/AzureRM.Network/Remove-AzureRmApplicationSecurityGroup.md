---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: b0387d10950073c4655c6e6015edc6957ae14edc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590733"
---
# <span data-ttu-id="31094-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="31094-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="31094-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31094-102">SYNOPSIS</span></span>
<span data-ttu-id="31094-103">Uygulama güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="31094-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31094-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31094-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31094-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="31094-105">DESCRIPTION</span></span>
<span data-ttu-id="31094-106">**Remove-AzureRmApplicationSecurityGroup** cmdlet 'i uygulama güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="31094-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="31094-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31094-107">EXAMPLES</span></span>

### <span data-ttu-id="31094-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="31094-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="31094-109">Bu komut MyResourceGroup adlı kaynak grubunda MyApplicationSecurityGrouo adlı bir uygulama güvenlik grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="31094-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="31094-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31094-110">PARAMETERS</span></span>

### <span data-ttu-id="31094-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31094-111">-DefaultProfile</span></span>
<span data-ttu-id="31094-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31094-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31094-113">-Force</span><span class="sxs-lookup"><span data-stu-id="31094-113">-Force</span></span>
<span data-ttu-id="31094-114">Kaynağı silmek istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="31094-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="31094-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="31094-115">-Name</span></span>
<span data-ttu-id="31094-116">Uygulama güvenlik grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="31094-116">The name of the application security group.</span></span>

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

### <span data-ttu-id="31094-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="31094-117">-PassThru</span></span>
<span data-ttu-id="31094-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="31094-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="31094-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="31094-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="31094-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31094-120">-ResourceGroupName</span></span>
<span data-ttu-id="31094-121">Uygulama güvenlik grubunun kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="31094-121">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="31094-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="31094-122">-Confirm</span></span>
<span data-ttu-id="31094-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="31094-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31094-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31094-124">-WhatIf</span></span>
<span data-ttu-id="31094-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="31094-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31094-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="31094-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31094-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31094-127">CommonParameters</span></span>
<span data-ttu-id="31094-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31094-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31094-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31094-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31094-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31094-130">INPUTS</span></span>

### <span data-ttu-id="31094-131">System. String</span><span class="sxs-lookup"><span data-stu-id="31094-131">System.String</span></span>

## <span data-ttu-id="31094-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31094-132">OUTPUTS</span></span>

### <span data-ttu-id="31094-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="31094-133">System.Object</span></span>

## <span data-ttu-id="31094-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31094-134">NOTES</span></span>

## <span data-ttu-id="31094-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31094-135">RELATED LINKS</span></span>

[<span data-ttu-id="31094-136">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="31094-136">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="31094-137">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="31094-137">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
