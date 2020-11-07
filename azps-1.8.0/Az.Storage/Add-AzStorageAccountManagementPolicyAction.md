---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: 73384827b5af2b3370eca1eee5a90066a89b8e55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758706"
---
# <span data-ttu-id="d4247-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="d4247-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="d4247-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4247-102">SYNOPSIS</span></span>
<span data-ttu-id="d4247-103">Giriş yönetim Ilkesi eylem grubu nesnesine bir eylem ekler veya eyleme sahip bir yönetim Ilkesi eylem grubu nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d4247-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="d4247-104">Nesne yeni-AzStorageAccountManagementPolicyRule 'da kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d4247-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="d4247-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4247-105">SYNTAX</span></span>

### <span data-ttu-id="d4247-106">BaseBlob (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d4247-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4247-107">Görüntü</span><span class="sxs-lookup"><span data-stu-id="d4247-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4247-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4247-108">DESCRIPTION</span></span>
<span data-ttu-id="d4247-109">**Add-AzStorageAccountManagementPolicyAction** cmdlet 'i, giriş Yönetim Ilkesi eylem grubu nesnesine bir eylem ekler veya eyleme sahip bir yönetim Ilkesi eylem grubu nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d4247-109">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="d4247-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4247-110">EXAMPLES</span></span>

### <span data-ttu-id="d4247-111">Örnek 1:4 eylemi olan bir ManagementPolicy eylem grubu nesnesi oluşturur, sonra bunu bir yönetim ilkesi kuralına ekleyin ve bir depolama hesabına ayarlayın</span><span class="sxs-lookup"><span data-stu-id="d4247-111">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="d4247-112">İlk komut yönetim Ilkesi eylem grubu nesnesi oluşturur, aşağıdaki 3 komut nesneye 3 eylem ekler.</span><span class="sxs-lookup"><span data-stu-id="d4247-112">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="d4247-113">Ardından bunu bir yönetim ilkesi kuralına ekleyin ve depolama hesabına ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d4247-113">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="d4247-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4247-114">PARAMETERS</span></span>

### <span data-ttu-id="d4247-115">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="d4247-115">-BaseBlobAction</span></span>
<span data-ttu-id="d4247-116">Baseblob için yönetim ilkesi eylemi.</span><span class="sxs-lookup"><span data-stu-id="d4247-116">The management policy action for baseblob.</span></span>

```yaml
Type: System.String
Parameter Sets: BaseBlob
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4247-117">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="d4247-117">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="d4247-118">Oluşturulduktan sonra gün cinsinden yaşı belirten tamsayı değeri.</span><span class="sxs-lookup"><span data-stu-id="d4247-118">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4247-119">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="d4247-119">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="d4247-120">Gün içinde son değişiklikten sonraki yaşı belirten tamsayı değeri.</span><span class="sxs-lookup"><span data-stu-id="d4247-120">Integer value indicating the age in days after last modification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BaseBlob
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4247-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4247-121">-DefaultProfile</span></span>
<span data-ttu-id="d4247-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4247-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4247-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4247-123">-InputObject</span></span>
<span data-ttu-id="d4247-124">ManagementPolicy eylem nesnesi girişi yapıyorsanız, eylemi giriş eylemi nesnesine ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d4247-124">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="d4247-125">Giriş yoksa, yeni bir eylem nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d4247-125">If not input, will create a new action object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4247-126">-Anlık, TAction</span><span class="sxs-lookup"><span data-stu-id="d4247-126">-SnapshotAction</span></span>
<span data-ttu-id="d4247-127">Anlık görüntü için yönetim ilkesi eylemi.</span><span class="sxs-lookup"><span data-stu-id="d4247-127">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4247-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4247-128">CommonParameters</span></span>
<span data-ttu-id="d4247-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4247-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4247-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4247-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4247-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4247-131">INPUTS</span></span>

### <span data-ttu-id="d4247-132">Microsoft. Azure. Commands. Management. Storage. model. PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="d4247-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="d4247-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4247-133">OUTPUTS</span></span>

### <span data-ttu-id="d4247-134">Microsoft. Azure. Commands. Management. Storage. model. PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="d4247-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="d4247-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4247-135">NOTES</span></span>

## <span data-ttu-id="d4247-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4247-136">RELATED LINKS</span></span>
