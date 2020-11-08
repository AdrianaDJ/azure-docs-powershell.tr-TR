---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
ms.openlocfilehash: 7a67d6aa0b891c78d644ec7d5f3923a354c3cef1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277727"
---
# <span data-ttu-id="d8f05-101">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d8f05-101">Get-AzManagedHsm</span></span>

## <span data-ttu-id="d8f05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8f05-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f05-103">Yönetilen HSMs alın.</span><span class="sxs-lookup"><span data-stu-id="d8f05-103">Get managed HSMs.</span></span>

## <span data-ttu-id="d8f05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8f05-104">SYNTAX</span></span>

```
Get-AzManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8f05-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8f05-105">DESCRIPTION</span></span>
<span data-ttu-id="d8f05-106">**Get-AzManagedHsm** cmdlet 'i, bir abonelikteki yönetilen hsms hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d8f05-106">The **Get-AzManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="d8f05-107">Tüm yönetilen HSMs örneklerini bir abonelikte görüntüleyebilir ya da sonuçlarınızı bir kaynak grubuna veya belirli bir yönetilen HSM 'ye göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8f05-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="d8f05-108">Tek bir yönetilen HSM aldığınızda bu cmdlet için kaynak grubu 'nun isteğe bağlı olduğunu belirten unutmayın, daha iyi performans için bunu yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="d8f05-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="d8f05-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8f05-109">EXAMPLES</span></span>

### <span data-ttu-id="d8f05-110">Örnek 1: geçerli aboneliğinizde tüm yönetilen HSMs 'leri edinin</span><span class="sxs-lookup"><span data-stu-id="d8f05-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="d8f05-111">Bu komut geçerli aboneliğinizde tüm yönetilen HSMs 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="d8f05-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="d8f05-112">Örnek 2: belirli bir yönetilen HSM alma</span><span class="sxs-lookup"><span data-stu-id="d8f05-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="d8f05-113">Bu komut, geçerli aboneliğinizde myhsm adlı yönetilen HSM 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="d8f05-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="d8f05-114">Örnek 3: kaynak grubunda yönetilen HSMs alma</span><span class="sxs-lookup"><span data-stu-id="d8f05-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="d8f05-115">Bu komut, myrg1 adlı kaynak grubundaki tüm yönetilen HSMs 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="d8f05-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="d8f05-116">Örnek 4: filtreleme kullanarak yönetilen HSMs alma</span><span class="sxs-lookup"><span data-stu-id="d8f05-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="d8f05-117">Bu komut, abonelikteki tüm yönetilen HSMs 'i "myhsm" ile başlayan bir alan alır.</span><span class="sxs-lookup"><span data-stu-id="d8f05-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="d8f05-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8f05-118">PARAMETERS</span></span>

### <span data-ttu-id="d8f05-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f05-119">-DefaultProfile</span></span>
<span data-ttu-id="d8f05-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8f05-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8f05-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8f05-121">-Name</span></span>
<span data-ttu-id="d8f05-122">HSM adı.</span><span class="sxs-lookup"><span data-stu-id="d8f05-122">HSM name.</span></span> <span data-ttu-id="d8f05-123">Cmdlet, adı ve seçili durumdaki ortamı temel alan bir HSM FQDN 'SI oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8f05-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8f05-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f05-124">-ResourceGroupName</span></span>
<span data-ttu-id="d8f05-125">Sorgulanan yönetilen HSM ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8f05-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8f05-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d8f05-126">-Tag</span></span>
<span data-ttu-id="d8f05-127">Yönetilen HSMs 'in listesini filtrelemek için belirtilen etiketin anahtarını ve isteğe bağlı değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8f05-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8f05-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f05-128">CommonParameters</span></span>
<span data-ttu-id="d8f05-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8f05-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f05-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d8f05-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f05-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8f05-131">INPUTS</span></span>

### <span data-ttu-id="d8f05-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d8f05-132">System.String</span></span>

### <span data-ttu-id="d8f05-133">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d8f05-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d8f05-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8f05-134">OUTPUTS</span></span>

### <span data-ttu-id="d8f05-135">Microsoft. Azure. Commands. Keykasa. modeller. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d8f05-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="d8f05-136">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultidentityıtem</span><span class="sxs-lookup"><span data-stu-id="d8f05-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="d8f05-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8f05-137">NOTES</span></span>

## <span data-ttu-id="d8f05-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8f05-138">RELATED LINKS</span></span>

[<span data-ttu-id="d8f05-139">Yeni-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d8f05-139">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="d8f05-140">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d8f05-140">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="d8f05-141">Güncelleştirme-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d8f05-141">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)