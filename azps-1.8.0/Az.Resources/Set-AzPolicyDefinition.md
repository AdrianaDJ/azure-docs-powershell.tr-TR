---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: f96ea5b7f36806378dff31cc81d211074638342c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759315"
---
# <span data-ttu-id="5d87f-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5d87f-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="5d87f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d87f-102">SYNOPSIS</span></span>
<span data-ttu-id="5d87f-103">İlke tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5d87f-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="5d87f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d87f-104">SYNTAX</span></span>

### <span data-ttu-id="5d87f-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5d87f-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d87f-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d87f-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d87f-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5d87f-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d87f-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="5d87f-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d87f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d87f-109">DESCRIPTION</span></span>
<span data-ttu-id="5d87f-110">**Set-AzPolicyDefinition** cmdlet 'i bir ilke tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5d87f-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="5d87f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d87f-111">EXAMPLES</span></span>

### <span data-ttu-id="5d87f-112">Örnek 1: ilke tanımının açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5d87f-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="5d87f-113">İlk komut, Get-AzPolicyDefinition cmdlet 'ini kullanarak VMPolicyDefinition adlı bir ilke tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="5d87f-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="5d87f-114">Komut bu nesneyi $PolicyDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5d87f-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="5d87f-115">İkinci komut $PolicyDefinition 'in **RESOURCEID** özelliği tarafından tanımlanan ilke tanımının açıklamasını günceller.</span><span class="sxs-lookup"><span data-stu-id="5d87f-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="5d87f-116">Örnek 2: ilke tanımının modunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5d87f-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="5d87f-117">Bu komut, VMPolicyDefinition adındaki ilke tanımını, Mode özelliğini ' All ' olarak ayarlamak için Set-AzPolicyDefinition cmdlet 'ini kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5d87f-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="5d87f-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d87f-118">PARAMETERS</span></span>

### <span data-ttu-id="5d87f-119">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="5d87f-119">-ApiVersion</span></span>
<span data-ttu-id="5d87f-120">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d87f-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5d87f-121">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="5d87f-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d87f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d87f-122">-DefaultProfile</span></span>
<span data-ttu-id="5d87f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5d87f-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d87f-124">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="5d87f-124">-Description</span></span>
<span data-ttu-id="5d87f-125">İlke tanımı için yeni bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d87f-125">Specifies a new description for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d87f-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5d87f-126">-DisplayName</span></span>
<span data-ttu-id="5d87f-127">İlke tanımı için yeni bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d87f-127">Specifies a new display name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d87f-128">-ID</span><span class="sxs-lookup"><span data-stu-id="5d87f-128">-Id</span></span>
<span data-ttu-id="5d87f-129">Bu cmdlet 'in değiştirdiği ilke tanımının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d87f-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d87f-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="5d87f-130">-ManagementGroupName</span></span>
<span data-ttu-id="5d87f-131">Güncelleştirilecek ilke tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5d87f-131">The name of the management group of the policy definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d87f-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5d87f-132">-Metadata</span></span>
<span data-ttu-id="5d87f-133">İlke tanımı için meta veriler.</span><span class="sxs-lookup"><span data-stu-id="5d87f-133">The metadata for policy definition.</span></span> <span data-ttu-id="5d87f-134">Bu, meta veri veya meta veri içeren bir dosya adının yolu olabilir.</span><span class="sxs-lookup"><span data-stu-id="5d87f-134">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d87f-135">-Mod</span><span class="sxs-lookup"><span data-stu-id="5d87f-135">-Mode</span></span>
<span data-ttu-id="5d87f-136">Yeni ilke tanımının modu.</span><span class="sxs-lookup"><span data-stu-id="5d87f-136">The mode of the new policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d87f-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="5d87f-137">-Name</span></span>
<span data-ttu-id="5d87f-138">Bu cmdlet 'in değiştirdiği ilke tanımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d87f-138">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d87f-139">-Parametre</span><span class="sxs-lookup"><span data-stu-id="5d87f-139">-Parameter</span></span>
<span data-ttu-id="5d87f-140">İlke tanımı için parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="5d87f-140">The parameters declaration for policy definition.</span></span> <span data-ttu-id="5d87f-141">Bu, parametre bildirimini içeren bir dosya adı veya URI veya dize olarak parametre bildirimi olabilir.</span><span class="sxs-lookup"><span data-stu-id="5d87f-141">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d87f-142">-İlke</span><span class="sxs-lookup"><span data-stu-id="5d87f-142">-Policy</span></span>
<span data-ttu-id="5d87f-143">İlke tanımı için yeni ilke kuralı belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d87f-143">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="5d87f-144">Bir. json dosyasının veya JavaScript nesne gösterimi (JSON) biçimindeki ilkeyi içeren dizenin yolunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5d87f-144">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d87f-145">-Pre-</span><span class="sxs-lookup"><span data-stu-id="5d87f-145">-Pre</span></span>
<span data-ttu-id="5d87f-146">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5d87f-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5d87f-147">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5d87f-147">-SubscriptionId</span></span>
<span data-ttu-id="5d87f-148">Güncelleştirilecek ilke tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5d87f-148">The subscription ID of the policy definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d87f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d87f-149">CommonParameters</span></span>
<span data-ttu-id="5d87f-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d87f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d87f-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d87f-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d87f-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d87f-152">INPUTS</span></span>

### <span data-ttu-id="5d87f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="5d87f-153">System.String</span></span>

### <span data-ttu-id="5d87f-154">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="5d87f-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5d87f-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d87f-155">OUTPUTS</span></span>

### <span data-ttu-id="5d87f-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5d87f-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5d87f-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d87f-157">NOTES</span></span>

## <span data-ttu-id="5d87f-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d87f-158">RELATED LINKS</span></span>

[<span data-ttu-id="5d87f-159">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5d87f-159">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="5d87f-160">Yeni-Azilketanımı</span><span class="sxs-lookup"><span data-stu-id="5d87f-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="5d87f-161">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5d87f-161">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


