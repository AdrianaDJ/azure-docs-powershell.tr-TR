---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 4f1c21f4f64193ec25a0392e094b8fd492ceba9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589768"
---
# <span data-ttu-id="61521-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="61521-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="61521-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61521-102">SYNOPSIS</span></span>
<span data-ttu-id="61521-103">IotHub anahtarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61521-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61521-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61521-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61521-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61521-105">DESCRIPTION</span></span>
<span data-ttu-id="61521-106">IotHub anahtarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61521-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="61521-107">Aynı ada sahip birden çok anahtar varsa, listede ilki kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="61521-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="61521-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61521-108">EXAMPLES</span></span>

### <span data-ttu-id="61521-109">Örnek 1 IotHub</span><span class="sxs-lookup"><span data-stu-id="61521-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="61521-110">İothubowner1 adındaki "myiothub" adındaki anahtarı kaldırır</span><span class="sxs-lookup"><span data-stu-id="61521-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="61521-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61521-111">PARAMETERS</span></span>

### <span data-ttu-id="61521-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61521-112">-DefaultProfile</span></span>
<span data-ttu-id="61521-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="61521-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61521-114">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="61521-114">-KeyName</span></span>
<span data-ttu-id="61521-115">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="61521-115">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61521-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="61521-116">-Name</span></span>
<span data-ttu-id="61521-117">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="61521-117">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61521-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61521-118">-ResourceGroupName</span></span>
<span data-ttu-id="61521-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="61521-119">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61521-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="61521-120">-Confirm</span></span>
<span data-ttu-id="61521-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61521-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61521-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61521-122">-WhatIf</span></span>
<span data-ttu-id="61521-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61521-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61521-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61521-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61521-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61521-125">CommonParameters</span></span>
<span data-ttu-id="61521-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61521-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61521-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61521-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61521-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61521-128">INPUTS</span></span>

### <span data-ttu-id="61521-129">System. String</span><span class="sxs-lookup"><span data-stu-id="61521-129">System.String</span></span>

## <span data-ttu-id="61521-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61521-130">OUTPUTS</span></span>

### <span data-ttu-id="61521-131">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="61521-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="61521-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61521-132">NOTES</span></span>

## <span data-ttu-id="61521-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61521-133">RELATED LINKS</span></span>

