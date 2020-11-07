---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 8b7603f145d45411b20b124823f28281d4117127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762220"
---
# <span data-ttu-id="968e7-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="968e7-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="968e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="968e7-102">SYNOPSIS</span></span>
<span data-ttu-id="968e7-103">IotHub anahtarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="968e7-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="968e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="968e7-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="968e7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="968e7-105">DESCRIPTION</span></span>
<span data-ttu-id="968e7-106">IotHub anahtarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="968e7-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="968e7-107">Aynı ada sahip birden çok anahtar varsa, listede ilki kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="968e7-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="968e7-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="968e7-108">EXAMPLES</span></span>

### <span data-ttu-id="968e7-109">Örnek 1 IotHub</span><span class="sxs-lookup"><span data-stu-id="968e7-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="968e7-110">İothubowner1 adındaki "myiothub" adındaki anahtarı kaldırır</span><span class="sxs-lookup"><span data-stu-id="968e7-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="968e7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="968e7-111">PARAMETERS</span></span>

### <span data-ttu-id="968e7-112">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="968e7-112">-KeyName</span></span>
<span data-ttu-id="968e7-113">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="968e7-113">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="968e7-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="968e7-114">-Name</span></span>
<span data-ttu-id="968e7-115">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="968e7-115">Name of the IotHub</span></span>

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

### <span data-ttu-id="968e7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="968e7-116">-ResourceGroupName</span></span>
<span data-ttu-id="968e7-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="968e7-117">Resource Group Name</span></span>

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

### <span data-ttu-id="968e7-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="968e7-118">-Confirm</span></span>
<span data-ttu-id="968e7-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="968e7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="968e7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="968e7-120">-WhatIf</span></span>
<span data-ttu-id="968e7-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="968e7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="968e7-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="968e7-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="968e7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="968e7-123">-DefaultProfile</span></span>
<span data-ttu-id="968e7-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="968e7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="968e7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="968e7-125">CommonParameters</span></span>
<span data-ttu-id="968e7-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="968e7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="968e7-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="968e7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="968e7-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="968e7-128">INPUTS</span></span>

### <span data-ttu-id="968e7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="968e7-129">System.String</span></span>

## <span data-ttu-id="968e7-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="968e7-130">OUTPUTS</span></span>

### <span data-ttu-id="968e7-131">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="968e7-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="968e7-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="968e7-132">NOTES</span></span>

## <span data-ttu-id="968e7-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="968e7-133">RELATED LINKS</span></span>

