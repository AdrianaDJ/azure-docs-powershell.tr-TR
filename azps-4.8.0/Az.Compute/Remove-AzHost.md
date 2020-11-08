---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 0d3f3a34257ad32c8b606b99c3f7170fb15684b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109115"
---
# <span data-ttu-id="1e5d6-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="1e5d6-101">Remove-AzHost</span></span>

## <span data-ttu-id="1e5d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e5d6-102">SYNOPSIS</span></span>
<span data-ttu-id="1e5d6-103">Ana bilgisayarı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1e5d6-103">Removes a host.</span></span>

## <span data-ttu-id="1e5d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e5d6-104">SYNTAX</span></span>

### <span data-ttu-id="1e5d6-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1e5d6-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e5d6-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="1e5d6-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e5d6-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="1e5d6-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e5d6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e5d6-108">DESCRIPTION</span></span>
<span data-ttu-id="1e5d6-109">Bu cmdlet bir ana bilgisayarı Silecek</span><span class="sxs-lookup"><span data-stu-id="1e5d6-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="1e5d6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e5d6-110">EXAMPLES</span></span>

### <span data-ttu-id="1e5d6-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1e5d6-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="1e5d6-112">Bu komut, verilen ana bilgisayarı alır ve kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1e5d6-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="1e5d6-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1e5d6-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="1e5d6-114">Bu komut, verilen ana bilgisayarı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1e5d6-114">This command removes the given host.</span></span>

## <span data-ttu-id="1e5d6-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e5d6-115">PARAMETERS</span></span>

### <span data-ttu-id="1e5d6-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="1e5d6-116">-AsJob</span></span>
<span data-ttu-id="1e5d6-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1e5d6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e5d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e5d6-118">-DefaultProfile</span></span>
<span data-ttu-id="1e5d6-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e5d6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e5d6-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="1e5d6-120">-HostGroupName</span></span>
<span data-ttu-id="1e5d6-121">Konak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1e5d6-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5d6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e5d6-122">-InputObject</span></span>
<span data-ttu-id="1e5d6-123">Konaktaki yerel nesne.</span><span class="sxs-lookup"><span data-stu-id="1e5d6-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5d6-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="1e5d6-124">-Name</span></span>
<span data-ttu-id="1e5d6-125">Ana bilgisayarın adı.</span><span class="sxs-lookup"><span data-stu-id="1e5d6-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5d6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e5d6-126">-ResourceGroupName</span></span>
<span data-ttu-id="1e5d6-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1e5d6-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5d6-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1e5d6-128">-ResourceId</span></span>
<span data-ttu-id="1e5d6-129">Kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1e5d6-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5d6-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="1e5d6-130">-Confirm</span></span>
<span data-ttu-id="1e5d6-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1e5d6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e5d6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e5d6-132">-WhatIf</span></span>
<span data-ttu-id="1e5d6-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e5d6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e5d6-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1e5d6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e5d6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e5d6-135">CommonParameters</span></span>
<span data-ttu-id="1e5d6-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e5d6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e5d6-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1e5d6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e5d6-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e5d6-138">INPUTS</span></span>

### <span data-ttu-id="1e5d6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1e5d6-139">System.String</span></span>

### <span data-ttu-id="1e5d6-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSHost</span><span class="sxs-lookup"><span data-stu-id="1e5d6-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="1e5d6-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e5d6-141">OUTPUTS</span></span>

### <span data-ttu-id="1e5d6-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="1e5d6-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="1e5d6-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e5d6-143">NOTES</span></span>

## <span data-ttu-id="1e5d6-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e5d6-144">RELATED LINKS</span></span>
