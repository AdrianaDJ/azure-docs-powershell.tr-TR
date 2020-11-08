---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: f6f12358e3182796f7665db4ee0b45cf42ea2c66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266741"
---
# <span data-ttu-id="eb857-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="eb857-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="eb857-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb857-102">SYNOPSIS</span></span>
<span data-ttu-id="eb857-103">Depolama hesabının tüm kullanıcı temsilci anahtarlarını iptal edin.</span><span class="sxs-lookup"><span data-stu-id="eb857-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="eb857-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb857-104">SYNTAX</span></span>

### <span data-ttu-id="eb857-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eb857-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb857-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="eb857-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb857-107">Accountresourceıd</span><span class="sxs-lookup"><span data-stu-id="eb857-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb857-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb857-108">DESCRIPTION</span></span>
<span data-ttu-id="eb857-109">**Revoke-AzStorageAccountUserDelegationKeys** cmdlet 'i, depolama hesabındaki tüm kimlik SAS belirteci de iptal edilecek.</span><span class="sxs-lookup"><span data-stu-id="eb857-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="eb857-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb857-110">EXAMPLES</span></span>

### <span data-ttu-id="eb857-111">Örnek 1: depolama hesabının tüm kullanıcı temsilci anahtarlarını Iptal etme</span><span class="sxs-lookup"><span data-stu-id="eb857-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="eb857-112">Bu örnekte, bir depolama hesabının tüm kullanıcı temsilci anahtarının iptal edildiği, kullanıcı temsilcisi anahtarlarından oluşturulan tüm kimlik SAS belirteçleri de iptal edilecek.</span><span class="sxs-lookup"><span data-stu-id="eb857-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="eb857-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb857-113">PARAMETERS</span></span>

### <span data-ttu-id="eb857-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb857-114">-DefaultProfile</span></span>
<span data-ttu-id="eb857-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eb857-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb857-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb857-116">-InputObject</span></span>
<span data-ttu-id="eb857-117">Get_AzStorageAccount, yeni-AzStorageAccount tarafından döndürülen bir depolama hesabı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="eb857-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb857-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="eb857-118">-PassThru</span></span>
<span data-ttu-id="eb857-119">Normalde bu cmdlet başarılı bir şekilde hiçbir çıkış döndürmez; Bu parametre cmdlet 'i başarılı bir şekilde bir değer döndürmesini zorlar ($true).</span><span class="sxs-lookup"><span data-stu-id="eb857-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="eb857-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb857-120">-ResourceGroupName</span></span>
<span data-ttu-id="eb857-121">Depolama hesabı kaynağını içeren kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="eb857-121">The resource group name containing the storage account resource.</span></span>

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

### <span data-ttu-id="eb857-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="eb857-122">-ResourceId</span></span>
<span data-ttu-id="eb857-123">Depolama hesabı kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="eb857-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases: StorageAccountResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb857-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="eb857-124">-StorageAccountName</span></span>
<span data-ttu-id="eb857-125">Depolama hesabı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="eb857-125">The name of the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb857-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="eb857-126">-Confirm</span></span>
<span data-ttu-id="eb857-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb857-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb857-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb857-128">-WhatIf</span></span>
<span data-ttu-id="eb857-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eb857-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb857-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eb857-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb857-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb857-131">CommonParameters</span></span>
<span data-ttu-id="eb857-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb857-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb857-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb857-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb857-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb857-134">INPUTS</span></span>

### <span data-ttu-id="eb857-135">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eb857-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="eb857-136">System. String</span><span class="sxs-lookup"><span data-stu-id="eb857-136">System.String</span></span>

## <span data-ttu-id="eb857-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb857-137">OUTPUTS</span></span>

### <span data-ttu-id="eb857-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb857-138">System.Boolean</span></span>

## <span data-ttu-id="eb857-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb857-139">NOTES</span></span>

## <span data-ttu-id="eb857-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb857-140">RELATED LINKS</span></span>
