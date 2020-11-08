---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: d7290d44a1e6a08b79ccb5a0b5ff88ec482b4875
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934206"
---
# <span data-ttu-id="846a2-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="846a2-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="846a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="846a2-102">SYNOPSIS</span></span>
<span data-ttu-id="846a2-103">Azure depolama hesabının yönetim ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="846a2-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="846a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="846a2-104">SYNTAX</span></span>

### <span data-ttu-id="846a2-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="846a2-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="846a2-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="846a2-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="846a2-107">Accountresourceıd</span><span class="sxs-lookup"><span data-stu-id="846a2-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="846a2-108">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="846a2-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="846a2-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="846a2-109">DESCRIPTION</span></span>
<span data-ttu-id="846a2-110">**Remove-AzStorageAccountManagementPolicy** cmdlet 'ı, Azure depolama hesabının yönetim ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="846a2-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="846a2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="846a2-111">EXAMPLES</span></span>

### <span data-ttu-id="846a2-112">Örnek 1: depolama hesabının yönetim ilkesini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="846a2-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="846a2-113">Bu komut, depolama hesabının yönetim ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="846a2-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="846a2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="846a2-114">PARAMETERS</span></span>

### <span data-ttu-id="846a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="846a2-115">-DefaultProfile</span></span>
<span data-ttu-id="846a2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="846a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="846a2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="846a2-117">-InputObject</span></span>
<span data-ttu-id="846a2-118">Kaldırılacak yönetim nesnesi</span><span class="sxs-lookup"><span data-stu-id="846a2-118">Management Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: PolicyObject
Aliases: ManagementPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="846a2-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="846a2-119">-PassThru</span></span>
<span data-ttu-id="846a2-120">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="846a2-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="846a2-121">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="846a2-121">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="846a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="846a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="846a2-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="846a2-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846a2-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="846a2-124">-StorageAccount</span></span>
<span data-ttu-id="846a2-125">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="846a2-125">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="846a2-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="846a2-126">-StorageAccountName</span></span>
<span data-ttu-id="846a2-127">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="846a2-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846a2-128">-Storageaccountresourceıd</span><span class="sxs-lookup"><span data-stu-id="846a2-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="846a2-129">Depolama hesabı kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="846a2-129">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="846a2-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="846a2-130">-Confirm</span></span>
<span data-ttu-id="846a2-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="846a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="846a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="846a2-132">-WhatIf</span></span>
<span data-ttu-id="846a2-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="846a2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="846a2-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="846a2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="846a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="846a2-135">CommonParameters</span></span>
<span data-ttu-id="846a2-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="846a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="846a2-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="846a2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="846a2-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="846a2-138">INPUTS</span></span>

### <span data-ttu-id="846a2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="846a2-139">System.String</span></span>

## <span data-ttu-id="846a2-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="846a2-140">OUTPUTS</span></span>

### <span data-ttu-id="846a2-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="846a2-141">System.Boolean</span></span>

## <span data-ttu-id="846a2-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="846a2-142">NOTES</span></span>

## <span data-ttu-id="846a2-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="846a2-143">RELATED LINKS</span></span>