---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c275ac087c24c58de73e72ac5dcf46839d710621
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916419"
---
# <span data-ttu-id="0cb04-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="0cb04-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="0cb04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cb04-102">SYNOPSIS</span></span>
<span data-ttu-id="0cb04-103">IotHub anahtarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0cb04-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="0cb04-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0cb04-104">SYNTAX</span></span>

```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cb04-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0cb04-105">DESCRIPTION</span></span>
<span data-ttu-id="0cb04-106">IotHub anahtarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0cb04-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="0cb04-107">Aynı ada sahip birden çok anahtar varsa, listede ilki kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="0cb04-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="0cb04-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0cb04-108">EXAMPLES</span></span>

### <span data-ttu-id="0cb04-109">Örnek 1 IotHub</span><span class="sxs-lookup"><span data-stu-id="0cb04-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="0cb04-110">İothubowner1 adındaki "myiothub" adındaki anahtarı kaldırır</span><span class="sxs-lookup"><span data-stu-id="0cb04-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="0cb04-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0cb04-111">PARAMETERS</span></span>

### <span data-ttu-id="0cb04-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cb04-112">-DefaultProfile</span></span>
<span data-ttu-id="0cb04-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0cb04-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cb04-114">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="0cb04-114">-KeyName</span></span>
<span data-ttu-id="0cb04-115">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="0cb04-115">Name of the Key</span></span>

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

### <span data-ttu-id="0cb04-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0cb04-116">-Name</span></span>
<span data-ttu-id="0cb04-117">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="0cb04-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="0cb04-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cb04-118">-ResourceGroupName</span></span>
<span data-ttu-id="0cb04-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0cb04-119">Resource Group Name</span></span>

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

### <span data-ttu-id="0cb04-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="0cb04-120">-Confirm</span></span>
<span data-ttu-id="0cb04-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0cb04-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cb04-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cb04-122">-WhatIf</span></span>
<span data-ttu-id="0cb04-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0cb04-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cb04-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0cb04-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cb04-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cb04-125">CommonParameters</span></span>
<span data-ttu-id="0cb04-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0cb04-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cb04-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cb04-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cb04-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0cb04-128">INPUTS</span></span>

### <span data-ttu-id="0cb04-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0cb04-129">System.String</span></span>

## <span data-ttu-id="0cb04-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0cb04-130">OUTPUTS</span></span>

### <span data-ttu-id="0cb04-131">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="0cb04-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="0cb04-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0cb04-132">NOTES</span></span>

## <span data-ttu-id="0cb04-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0cb04-133">RELATED LINKS</span></span>
