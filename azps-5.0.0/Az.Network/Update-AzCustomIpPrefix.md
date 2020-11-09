---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325165"
---
# <span data-ttu-id="bf362-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="bf362-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="bf362-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf362-102">SYNOPSIS</span></span>
<span data-ttu-id="bf362-103">Custobir önek güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="bf362-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="bf362-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf362-104">SYNTAX</span></span>

### <span data-ttu-id="bf362-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf362-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf362-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf362-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf362-107">Updatebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="bf362-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf362-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf362-108">DESCRIPTION</span></span>
<span data-ttu-id="bf362-109">**Update-Azcustomı önek** cmdlet 'i, kullanıcının customı önekini komisyon veya yetkisini almasına olanak tanır ya da kaynağın etiketlerini düzenler.</span><span class="sxs-lookup"><span data-stu-id="bf362-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="bf362-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf362-110">EXAMPLES</span></span>

### <span data-ttu-id="bf362-111">Örnek 1: özelmi önekini komisyon</span><span class="sxs-lookup"><span data-stu-id="bf362-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="bf362-112">Yukarıdaki komut, Custombu önekinin komisyonsiz işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="bf362-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="bf362-113">Örnek 2: özelmi önekini yetki alma</span><span class="sxs-lookup"><span data-stu-id="bf362-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="bf362-114">Yukarıdaki komut, Custombu önekinin ön komisyonlandırma işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="bf362-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="bf362-115">Örnek 3: Custolerlerönek öneki</span><span class="sxs-lookup"><span data-stu-id="bf362-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="bf362-116">Yukarıdaki komut, Custolerlerönek önekinin etiketlerini güncelleştirecek.</span><span class="sxs-lookup"><span data-stu-id="bf362-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="bf362-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf362-117">PARAMETERS</span></span>

### <span data-ttu-id="bf362-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="bf362-118">-AsJob</span></span>
<span data-ttu-id="bf362-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bf362-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf362-120">-Komisyon</span><span class="sxs-lookup"><span data-stu-id="bf362-120">-Commission</span></span>
<span data-ttu-id="bf362-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bf362-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf362-122">-Dekombinasyon</span><span class="sxs-lookup"><span data-stu-id="bf362-122">-Decomission</span></span>
<span data-ttu-id="bf362-123">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bf362-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf362-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf362-124">-DefaultProfile</span></span>
<span data-ttu-id="bf362-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf362-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf362-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf362-126">-InputObject</span></span>
<span data-ttu-id="bf362-127">Ayarlanacak özel.</span><span class="sxs-lookup"><span data-stu-id="bf362-127">The CustomIpPrefix to set.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf362-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf362-128">-Name</span></span>
<span data-ttu-id="bf362-129">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="bf362-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf362-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf362-130">-ResourceGroupName</span></span>
<span data-ttu-id="bf362-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bf362-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf362-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bf362-132">-ResourceId</span></span>
<span data-ttu-id="bf362-133">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="bf362-133">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf362-134">Etiketli</span><span class="sxs-lookup"><span data-stu-id="bf362-134">-Tag</span></span>
<span data-ttu-id="bf362-135">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="bf362-135">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: SetByInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf362-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="bf362-136">-Confirm</span></span>
<span data-ttu-id="bf362-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bf362-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf362-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf362-138">-WhatIf</span></span>
<span data-ttu-id="bf362-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf362-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf362-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bf362-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf362-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf362-141">CommonParameters</span></span>
<span data-ttu-id="bf362-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf362-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf362-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bf362-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf362-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf362-144">INPUTS</span></span>

### <span data-ttu-id="bf362-145">System. String</span><span class="sxs-lookup"><span data-stu-id="bf362-145">System.String</span></span>

### <span data-ttu-id="bf362-146">Microsoft. Azure. Commands. Network. model. Pscustolermi öneki</span><span class="sxs-lookup"><span data-stu-id="bf362-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="bf362-147">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bf362-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bf362-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf362-148">OUTPUTS</span></span>

### <span data-ttu-id="bf362-149">Microsoft. Azure. Commands. Network. model. Pscustolermi öneki</span><span class="sxs-lookup"><span data-stu-id="bf362-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="bf362-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf362-150">NOTES</span></span>

## <span data-ttu-id="bf362-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf362-151">RELATED LINKS</span></span>

[<span data-ttu-id="bf362-152">Get-Azözelmi öneki</span><span class="sxs-lookup"><span data-stu-id="bf362-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="bf362-153">Yeni-Azözelmi öneki</span><span class="sxs-lookup"><span data-stu-id="bf362-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="bf362-154">Remove-Azcustomhttp öneki</span><span class="sxs-lookup"><span data-stu-id="bf362-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)