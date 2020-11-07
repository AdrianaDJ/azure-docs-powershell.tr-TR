---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 0f3a6bfa99a199a737c7a69d151d29f5918cc502
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593112"
---
# <span data-ttu-id="5e008-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="5e008-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="5e008-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e008-102">SYNOPSIS</span></span>
<span data-ttu-id="5e008-103">Bir IotHub siler.</span><span class="sxs-lookup"><span data-stu-id="5e008-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e008-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e008-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e008-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e008-105">DESCRIPTION</span></span>
<span data-ttu-id="5e008-106">Bir IotHub siler.</span><span class="sxs-lookup"><span data-stu-id="5e008-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="5e008-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e008-107">EXAMPLES</span></span>

### <span data-ttu-id="5e008-108">Örnek 1 IotHub</span><span class="sxs-lookup"><span data-stu-id="5e008-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="5e008-109">"Myiothub" adındaki bir IotHub kaldırır</span><span class="sxs-lookup"><span data-stu-id="5e008-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="5e008-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e008-110">PARAMETERS</span></span>

### <span data-ttu-id="5e008-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="5e008-111">-Name</span></span>
<span data-ttu-id="5e008-112">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="5e008-112">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e008-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e008-113">-ResourceGroupName</span></span>
<span data-ttu-id="5e008-114">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5e008-114">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e008-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="5e008-115">-Confirm</span></span>
<span data-ttu-id="5e008-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5e008-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e008-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e008-117">-WhatIf</span></span>
<span data-ttu-id="5e008-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e008-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e008-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5e008-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e008-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e008-120">-DefaultProfile</span></span>
<span data-ttu-id="5e008-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e008-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e008-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e008-122">CommonParameters</span></span>
<span data-ttu-id="5e008-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e008-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e008-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e008-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e008-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e008-125">INPUTS</span></span>

### <span data-ttu-id="5e008-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5e008-126">System.String</span></span>

## <span data-ttu-id="5e008-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e008-127">OUTPUTS</span></span>

### <span data-ttu-id="5e008-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="5e008-128">System.Object</span></span>

## <span data-ttu-id="5e008-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e008-129">NOTES</span></span>

## <span data-ttu-id="5e008-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e008-130">RELATED LINKS</span></span>
