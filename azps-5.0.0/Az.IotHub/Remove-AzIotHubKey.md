---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c50ee56a5dcb15c3b199e9aaf08aeca74828cc66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275323"
---
# <span data-ttu-id="658f8-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="658f8-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="658f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="658f8-102">SYNOPSIS</span></span>
<span data-ttu-id="658f8-103">IotHub anahtarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="658f8-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="658f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="658f8-104">SYNTAX</span></span>

### <span data-ttu-id="658f8-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="658f8-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="658f8-106">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="658f8-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="658f8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="658f8-107">DESCRIPTION</span></span>
<span data-ttu-id="658f8-108">IotHub anahtarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="658f8-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="658f8-109">Aynı ada sahip birden çok anahtar varsa, listede ilki kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="658f8-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="658f8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="658f8-110">EXAMPLES</span></span>

### <span data-ttu-id="658f8-111">Örnek 1 IotHub</span><span class="sxs-lookup"><span data-stu-id="658f8-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="658f8-112">İothubowner1 adındaki "myiothub" adındaki anahtarı kaldırır</span><span class="sxs-lookup"><span data-stu-id="658f8-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="658f8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="658f8-113">PARAMETERS</span></span>

### <span data-ttu-id="658f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="658f8-114">-DefaultProfile</span></span>
<span data-ttu-id="658f8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="658f8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="658f8-116">-Hubıd</span><span class="sxs-lookup"><span data-stu-id="658f8-116">-HubId</span></span>
<span data-ttu-id="658f8-117">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="658f8-117">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="658f8-118">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="658f8-118">-KeyName</span></span>
<span data-ttu-id="658f8-119">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="658f8-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="658f8-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="658f8-120">-Name</span></span>
<span data-ttu-id="658f8-121">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="658f8-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="658f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="658f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="658f8-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="658f8-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="658f8-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="658f8-124">-Confirm</span></span>
<span data-ttu-id="658f8-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="658f8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="658f8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="658f8-126">-WhatIf</span></span>
<span data-ttu-id="658f8-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="658f8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="658f8-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="658f8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="658f8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="658f8-129">CommonParameters</span></span>
<span data-ttu-id="658f8-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="658f8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="658f8-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="658f8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="658f8-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="658f8-132">INPUTS</span></span>

### <span data-ttu-id="658f8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="658f8-133">System.String</span></span>

## <span data-ttu-id="658f8-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="658f8-134">OUTPUTS</span></span>

### <span data-ttu-id="658f8-135">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="658f8-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="658f8-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="658f8-136">NOTES</span></span>

## <span data-ttu-id="658f8-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="658f8-137">RELATED LINKS</span></span>
