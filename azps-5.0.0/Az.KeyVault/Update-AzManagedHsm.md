---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsm.md
ms.openlocfilehash: 49e8e5aeddba1b15c97155a200413ea774c8a7a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280187"
---
# <span data-ttu-id="75dac-101">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="75dac-101">Update-AzManagedHsm</span></span>

## <span data-ttu-id="75dac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75dac-102">SYNOPSIS</span></span>
<span data-ttu-id="75dac-103">Azure Managed HSM 'in durumunu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="75dac-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="75dac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75dac-104">SYNTAX</span></span>

### <span data-ttu-id="75dac-105">UpdateByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="75dac-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75dac-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75dac-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75dac-107">Updatebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="75dac-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75dac-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="75dac-108">DESCRIPTION</span></span>
<span data-ttu-id="75dac-109">Bu cmdlet, bir Azure yönetilen HSM durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="75dac-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="75dac-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75dac-110">EXAMPLES</span></span>

### <span data-ttu-id="75dac-111">Örnek 1: yönetilen HSM 'yi doğrudan güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="75dac-111">Example 1: Update a managed Hsm directly</span></span>
```powershell
PS C:\> Update-AzManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName -Tag @{testKey="testValue"} | fl

Managed HSM Name                    : testmhsm
Resource Group Name                 : testmhsm
Location                            : eastus2euap
Resource ID                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testmhsm/provid
                                      ers/Microsoft.KeyVault/managedHSMs/testmhsm
HSM Pool URI                        :
Tenant ID                           : xxxxxx-xxxx-xxxx-xxxxxxxxxxxx
Initial Admin Object Ids            : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SKU                                 : StandardB1
Soft Delete Enabled?                : True
Enabled Purge Protection?           : False
Soft Delete Retention Period (days) : 90
Provisioning State                  : Provisioning
Status Message                      : Resource creation in progress. Starting service...
Tags                                :
                                      Name        Value
                                      ====        =====
                                      testKey     testValued
```

<span data-ttu-id="75dac-112">Kaynak grubunda adı geçen yönetilen HSM 'deki etiketleri güncelleştirir `$hsmName` `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="75dac-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="75dac-113">Örnek 2: boru kullanarak yönetilen bir HSM 'yi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="75dac-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="75dac-114">Boru söz dizimini kullanarak yönetilen HSM 'deki etiketleri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="75dac-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="75dac-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75dac-115">PARAMETERS</span></span>

### <span data-ttu-id="75dac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75dac-116">-DefaultProfile</span></span>
<span data-ttu-id="75dac-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75dac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75dac-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75dac-118">-InputObject</span></span>
<span data-ttu-id="75dac-119">Yönetilen HSM nesnesi.</span><span class="sxs-lookup"><span data-stu-id="75dac-119">Managed HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75dac-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="75dac-120">-Name</span></span>
<span data-ttu-id="75dac-121">Yönetilen HSM adı.</span><span class="sxs-lookup"><span data-stu-id="75dac-121">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75dac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75dac-122">-ResourceGroupName</span></span>
<span data-ttu-id="75dac-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="75dac-123">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75dac-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="75dac-124">-ResourceId</span></span>
<span data-ttu-id="75dac-125">Yönetilen HSM 'nin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="75dac-125">Resource ID of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75dac-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="75dac-126">-Tag</span></span>
<span data-ttu-id="75dac-127">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="75dac-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="75dac-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="75dac-128">-Confirm</span></span>
<span data-ttu-id="75dac-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="75dac-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75dac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75dac-130">-WhatIf</span></span>
<span data-ttu-id="75dac-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75dac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75dac-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="75dac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75dac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75dac-133">CommonParameters</span></span>
<span data-ttu-id="75dac-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75dac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75dac-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="75dac-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75dac-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75dac-136">INPUTS</span></span>

### <span data-ttu-id="75dac-137">Microsoft. Azure. Commands. Keykasa. modeller. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="75dac-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="75dac-138">System. String</span><span class="sxs-lookup"><span data-stu-id="75dac-138">System.String</span></span>

### <span data-ttu-id="75dac-139">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="75dac-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="75dac-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75dac-140">OUTPUTS</span></span>

### <span data-ttu-id="75dac-141">Microsoft. Azure. Commands. Keykasa. modeller. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="75dac-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="75dac-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75dac-142">NOTES</span></span>

## <span data-ttu-id="75dac-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75dac-143">RELATED LINKS</span></span>

[<span data-ttu-id="75dac-144">Yeni-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="75dac-144">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="75dac-145">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="75dac-145">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="75dac-146">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="75dac-146">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)