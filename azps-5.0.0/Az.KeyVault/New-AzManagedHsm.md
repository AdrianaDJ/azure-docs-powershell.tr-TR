---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
ms.openlocfilehash: 2cab0fedd31f482b2e826a02f686ec8bf651c1bb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280210"
---
# <span data-ttu-id="0576e-101">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0576e-101">New-AzManagedHsm</span></span>

## <span data-ttu-id="0576e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0576e-102">SYNOPSIS</span></span>
<span data-ttu-id="0576e-103">Yönetilen bir HSM oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0576e-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="0576e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0576e-104">SYNTAX</span></span>

```
New-AzManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0576e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0576e-105">DESCRIPTION</span></span>
<span data-ttu-id="0576e-106">**Yeni-AzManagedHsm** cmdlet 'i belirtilen kaynak grubunda YÖNETILEN bir HSM oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0576e-106">The **New-AzManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="0576e-107">Yönetilen HSM 'de anahtar eklemek, kaldırmak veya listelemek için, kullanıcının yönetici 'ye Kullanıcı KIMLIĞI ekleyerek izinleri vermesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="0576e-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="0576e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0576e-108">EXAMPLES</span></span>

### <span data-ttu-id="0576e-109">Örnek 1: StandardB1 yönetimli bir HSM oluşturma</span><span class="sxs-lookup"><span data-stu-id="0576e-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="0576e-110">Bu komut, eastus2euap konumunda myhsm adlı bir yönetilen HSM oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0576e-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="0576e-111">Komut, yönetilen HSM 'yi myrg1 adlı kaynak grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="0576e-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="0576e-112">Komut, *SKU* parametresi için bir değer belirtmediğinden, Standard_B1 YÖNETIMLI bir HSM oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0576e-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="0576e-113">Örnek 2: CustomB32 yönetimli bir HSM oluşturma</span><span class="sxs-lookup"><span data-stu-id="0576e-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="0576e-114">Bu komut, önceki örnekte olduğu gibi, yönetilen bir HSM oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0576e-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="0576e-115">Bununla birlikte, CustomB32 yönetimli bir HSM oluşturmak için *SKU* parametre CustomB32 değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0576e-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="0576e-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0576e-116">PARAMETERS</span></span>

### <span data-ttu-id="0576e-117">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="0576e-117">-Administrator</span></span>
<span data-ttu-id="0576e-118">Bu yönetilen HSM havuzu için ilk yönetici nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="0576e-118">Initial administrator object id for this managed HSM pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0576e-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="0576e-119">-AsJob</span></span>
<span data-ttu-id="0576e-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0576e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0576e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0576e-121">-DefaultProfile</span></span>
<span data-ttu-id="0576e-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0576e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0576e-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="0576e-123">-Location</span></span>
<span data-ttu-id="0576e-124">Anahtar Kasası oluşturacağınız Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0576e-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="0576e-125">Seçimlerinizi görmek için komut Get-AzResourceProvider ProviderNamespace parametresiyle birlikte kullanın.</span><span class="sxs-lookup"><span data-stu-id="0576e-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="0576e-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="0576e-126">-Name</span></span>
<span data-ttu-id="0576e-127">Oluşturulacak yönetilen HSM 'in adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0576e-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="0576e-128">Ad, harf, sayı veya kısa çizgi bileşimleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="0576e-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="0576e-129">Ad bir harfle veya rakamla başlamalıdır ve bitmelidir.</span><span class="sxs-lookup"><span data-stu-id="0576e-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="0576e-130">Ad, evrensel olarak benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0576e-130">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0576e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0576e-131">-ResourceGroupName</span></span>
<span data-ttu-id="0576e-132">Anahtar Kasası oluşturulacak varolan bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0576e-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="0576e-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="0576e-133">-Sku</span></span>
<span data-ttu-id="0576e-134">Yönetilen HSM örneğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0576e-134">Specifies the SKU of the managed HSM instance.</span></span>

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

### <span data-ttu-id="0576e-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0576e-135">-Tag</span></span>
<span data-ttu-id="0576e-136">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="0576e-136">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0576e-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="0576e-137">-Confirm</span></span>
<span data-ttu-id="0576e-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0576e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0576e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0576e-139">-WhatIf</span></span>
<span data-ttu-id="0576e-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0576e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0576e-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0576e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0576e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0576e-142">CommonParameters</span></span>
<span data-ttu-id="0576e-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0576e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0576e-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0576e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0576e-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0576e-145">INPUTS</span></span>

### <span data-ttu-id="0576e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0576e-146">System.String</span></span>

### <span data-ttu-id="0576e-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="0576e-147">System.String[]</span></span>

### <span data-ttu-id="0576e-148">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0576e-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0576e-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0576e-149">OUTPUTS</span></span>

### <span data-ttu-id="0576e-150">Microsoft. Azure. Commands. Keykasa. modeller. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0576e-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="0576e-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0576e-151">NOTES</span></span>

## <span data-ttu-id="0576e-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0576e-152">RELATED LINKS</span></span>

[<span data-ttu-id="0576e-153">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0576e-153">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)

[<span data-ttu-id="0576e-154">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0576e-154">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="0576e-155">Güncelleştirme-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0576e-155">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)