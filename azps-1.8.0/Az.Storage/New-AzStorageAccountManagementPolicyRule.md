---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: 195ef931b942f3dc8a88ede7e3feb31a3b8aa77f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758626"
---
# <span data-ttu-id="76ec0-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="76ec0-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="76ec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="76ec0-103">Set-AzStorageAccountManagementPolicy 'de kullanılabilen bir ManagementPolicy kural nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76ec0-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="76ec0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76ec0-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76ec0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="76ec0-105">DESCRIPTION</span></span>
<span data-ttu-id="76ec0-106">**New-AzStorageAccountManagementPolicyRule** cmdlet 'i set-azstorageaccountmanagementpolicy 'de kullanılabilen bir managementpolicy kural nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76ec0-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="76ec0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76ec0-107">EXAMPLES</span></span>

### <span data-ttu-id="76ec0-108">Örnek 1: yönetim Ilkesi kural nesnesi oluşturur ve bir depolama hesabına ayarlanır</span><span class="sxs-lookup"><span data-stu-id="76ec0-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2

PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name rule1 -Action $action -Filter $filter
PS C:\>$rule

Enabled    : True
Name       : rule1
Definition : {
                 "Actions":  {
                                 "BaseBlob":  {
                                                  "TierToCool":  {
                                                                     "DaysAfterModificationGreaterThan":  30
                                                                 },
                                                  "TierToArchive":  {
                                                                        "DaysAfterModificationGreaterThan":  50
                                                                    },
                                                  "Delete":  {
                                                                 "DaysAfterModificationGreaterThan":  100
                                                             }
                                              },
                                 "Snapshot":  {
                                                  "Delete":  {
                                                                 "DaysAfterCreationGreaterThan":  100
                                                             }
                                              }
                             },
                 "Filters":  {
                                 "PrefixMatch":  [
                                                     "blobprefix1",
                                                     "blobprefix2"
                                                 ],
                                 "BlobTypes":  [
                                                   "blockBlob"
                                               ]
                             }
             }

PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="76ec0-109">Bu komut, yönetim ilkesi eylem grubu nesnesi için 4 eylem ve ManagementPolicy Rule Filter nesnesi içeren bir ManagementPolicy kural nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="76ec0-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="76ec0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76ec0-110">PARAMETERS</span></span>

### <span data-ttu-id="76ec0-111">-Eylem</span><span class="sxs-lookup"><span data-stu-id="76ec0-111">-Action</span></span>
<span data-ttu-id="76ec0-112">Eylem kümesini tanımlayan bir nesne.</span><span class="sxs-lookup"><span data-stu-id="76ec0-112">An object that defines the action set.</span></span>
<span data-ttu-id="76ec0-113">Nesne cmdlet Add-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="76ec0-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76ec0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ec0-114">-DefaultProfile</span></span>
<span data-ttu-id="76ec0-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76ec0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76ec0-116">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="76ec0-116">-Disabled</span></span>
<span data-ttu-id="76ec0-117">Ayarlanmışsa kural devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="76ec0-117">The rule is disabled if set it.</span></span>

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

### <span data-ttu-id="76ec0-118">-Filtre</span><span class="sxs-lookup"><span data-stu-id="76ec0-118">-Filter</span></span>
<span data-ttu-id="76ec0-119">Filtre kümesini tanımlayan bir nesne.</span><span class="sxs-lookup"><span data-stu-id="76ec0-119">An object that defines the filter set.</span></span>
<span data-ttu-id="76ec0-120">Nesne cmdlet New-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="76ec0-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76ec0-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="76ec0-121">-Name</span></span>
<span data-ttu-id="76ec0-122">Kural adı alfa sayısal karakterlerinin herhangi bir birleşimini içerebilir.</span><span class="sxs-lookup"><span data-stu-id="76ec0-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="76ec0-123">Kural adı büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="76ec0-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="76ec0-124">Bir ilke içinde benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="76ec0-124">It must be unique within a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ec0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ec0-125">CommonParameters</span></span>
<span data-ttu-id="76ec0-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76ec0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ec0-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76ec0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ec0-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76ec0-128">INPUTS</span></span>

### <span data-ttu-id="76ec0-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="76ec0-129">None</span></span>

## <span data-ttu-id="76ec0-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76ec0-130">OUTPUTS</span></span>

### <span data-ttu-id="76ec0-131">Microsoft. Azure. Commands. Management. Storage. model. PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="76ec0-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="76ec0-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76ec0-132">NOTES</span></span>

## <span data-ttu-id="76ec0-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76ec0-133">RELATED LINKS</span></span>
