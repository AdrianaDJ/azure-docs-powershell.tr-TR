---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/set-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 6a5b97ca21ca08ba51a96528e5652e80d71aef07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758547"
---
# <span data-ttu-id="ee6c5-101">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ee6c5-101">Set-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="ee6c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ee6c5-103">Azure depolama hesabının yönetim ilkesini oluşturur veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-103">Creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="ee6c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee6c5-104">SYNTAX</span></span>

### <span data-ttu-id="ee6c5-105">AccountNamePolicyRule (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ee6c5-105">AccountNamePolicyRule (Default)</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Rule <PSManagementPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee6c5-106">AccountNamePolicyObject</span><span class="sxs-lookup"><span data-stu-id="ee6c5-106">AccountNamePolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Policy <PSManagementPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee6c5-107">AccountObjectPolicyRule</span><span class="sxs-lookup"><span data-stu-id="ee6c5-107">AccountObjectPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee6c5-108">AccountObjectPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ee6c5-108">AccountObjectPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee6c5-109">Accountresourceıdpolicyrule</span><span class="sxs-lookup"><span data-stu-id="ee6c5-109">AccountResourceIdPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee6c5-110">Accountresourceıdpolicyobject</span><span class="sxs-lookup"><span data-stu-id="ee6c5-110">AccountResourceIdPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee6c5-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee6c5-111">DESCRIPTION</span></span>
<span data-ttu-id="ee6c5-112">**Set-AzStorageAccountManagementPolicy** cmdlet 'i, bir Azure depolama hesabının yönetim ilkesini oluşturur veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-112">The **Set-AzStorageAccountManagementPolicy** cmdlet creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="ee6c5-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee6c5-113">EXAMPLES</span></span>

### <span data-ttu-id="ee6c5-114">Örnek 1: yönetim ilkesi kural nesneleri olan bir depolama hesabının yönetim ilkesini oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-114">Example 1: Create or update the management policy of a Storage account with ManagementPolicy rule objects.</span></span>
```
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -SnapshotAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$filter1 = New-AzStorageAccountManagementPolicyFilter -PrefixMatch ab,cd 
PS C:\>$rule1 = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action1 -Filter $filter1

PS C:\>$action2 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$filter2 = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule2 = New-AzStorageAccountManagementPolicyRule -Name Test2 -Action $action2 -Filter $filter2

PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule1,$rule2


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:29:29 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
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
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="ee6c5-115">Bu komut önce 2 Yönetim Ilkesi kural nesneleri oluşturur, ardından 2 ManagementPolicy kural nesneleriyle bir depolama hesabının yönetim ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-115">This command first create 2 ManagementPolicy rule objects, then creates or updates the management policy of a Storage account with the 2 ManagementPolicy rule objects.</span></span>

### <span data-ttu-id="ee6c5-116">Örnek 2: JSON biçim ilkesiyle depolama hesabının yönetim ilkesini oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-116">Example 2: Create or update the management policy of a Storage account with a Json format policy.</span></span>
```
PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Policy (@{
    Rules=(@{
        Enabled="true";
        Name="Test";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=30;
                    TierToArchive=50;
                    Delete=100;
                });
                Snapshot=(@{
                    Delete=100
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
                PrefixMatch=@("prefix1","prefix2");
            })
        })
    },
    @{
        Enabled="false";
        Name="Test2";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=80;
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
            })
        })
    })
})


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:24:55 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
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
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  80
                                                                                                },
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  null
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="ee6c5-117">Bu komut, JSON biçim ilkesiyle depolama hesabının yönetim ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-117">This command creates or updates the management policy of a Storage account with a json format policy.</span></span>

### <span data-ttu-id="ee6c5-118">Örnek 3: depolama hesabından yönetim ilkesini alın ve sonra bunu başka bir depolama hesabına ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-118">Example 3: Get the management policy from a Storage account, then set it to another Storage account.</span></span>
```
PS C:\>$outputPolicy = Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" | Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup2" -AccountName "mystorageaccount2"
```

<span data-ttu-id="ee6c5-119">Bu komut önce bir depolama hesabındaki yönetim ilkesini alır, ardından başka bir depolama hesabına ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-119">This command first gets the management policy from a Storage account, then set it to another Storage account.</span></span>

## <span data-ttu-id="ee6c5-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee6c5-120">PARAMETERS</span></span>

### <span data-ttu-id="ee6c5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee6c5-121">-DefaultProfile</span></span>
<span data-ttu-id="ee6c5-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee6c5-123">-İlke</span><span class="sxs-lookup"><span data-stu-id="ee6c5-123">-Policy</span></span>
<span data-ttu-id="ee6c5-124">Ayarlanacak yönetim Ilkesi nesnesi</span><span class="sxs-lookup"><span data-stu-id="ee6c5-124">Management Policy Object to Set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: AccountNamePolicyObject, AccountObjectPolicyObject, AccountResourceIdPolicyObject
Aliases: ManagementPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee6c5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee6c5-125">-ResourceGroupName</span></span>
<span data-ttu-id="ee6c5-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee6c5-127">-Kural</span><span class="sxs-lookup"><span data-stu-id="ee6c5-127">-Rule</span></span>
<span data-ttu-id="ee6c5-128">Yönetim Ilkesi kuralları.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-128">The Management Policy rules.</span></span> <span data-ttu-id="ee6c5-129">Nesneye New-AzStorageAccountManagementPolicyRule cmdlet ile erişin.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-129">Get the object with New-AzStorageAccountManagementPolicyRule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule[]
Parameter Sets: AccountNamePolicyRule, AccountObjectPolicyRule, AccountResourceIdPolicyRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee6c5-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee6c5-130">-StorageAccount</span></span>
<span data-ttu-id="ee6c5-131">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="ee6c5-131">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectPolicyRule, AccountObjectPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee6c5-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ee6c5-132">-StorageAccountName</span></span>
<span data-ttu-id="ee6c5-133">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-133">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee6c5-134">-Storageaccountresourceıd</span><span class="sxs-lookup"><span data-stu-id="ee6c5-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="ee6c5-135">Depolama hesabı kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-135">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceIdPolicyRule, AccountResourceIdPolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee6c5-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="ee6c5-136">-Confirm</span></span>
<span data-ttu-id="ee6c5-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee6c5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee6c5-138">-WhatIf</span></span>
<span data-ttu-id="ee6c5-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee6c5-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee6c5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee6c5-141">CommonParameters</span></span>
<span data-ttu-id="ee6c5-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee6c5-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee6c5-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee6c5-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee6c5-144">INPUTS</span></span>

### <span data-ttu-id="ee6c5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ee6c5-145">System.String</span></span>

## <span data-ttu-id="ee6c5-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee6c5-146">OUTPUTS</span></span>

### <span data-ttu-id="ee6c5-147">Microsoft. Azure. Commands. Management. Storage. model. PSManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ee6c5-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span></span>

## <span data-ttu-id="ee6c5-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee6c5-148">NOTES</span></span>

## <span data-ttu-id="ee6c5-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee6c5-149">RELATED LINKS</span></span>