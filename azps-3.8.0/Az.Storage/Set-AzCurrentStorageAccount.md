---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: c57f8a7ce6b4f7275e724c777c2e6dfd54a680ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098536"
---
# <span data-ttu-id="7efd8-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7efd8-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="7efd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7efd8-102">SYNOPSIS</span></span>
<span data-ttu-id="7efd8-103">Belirtilen aboneliğin geçerli depolama hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7efd8-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="7efd8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7efd8-104">SYNTAX</span></span>

### <span data-ttu-id="7efd8-105">UsingResourceGroupAndNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7efd8-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7efd8-106">Storagecontext 'i</span><span class="sxs-lookup"><span data-stu-id="7efd8-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7efd8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7efd8-107">DESCRIPTION</span></span>
<span data-ttu-id="7efd8-108">**Set-AzCurrentStorageAccount** cmdlet 'ı, Azure PowerShell 'de belirtilen Azure aboneliğinin geçerli Azure Depolama hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7efd8-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="7efd8-109">Depolama hesabı adı belirtmeden depolama alanına eriştiğinizde geçerli depolama hesabı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7efd8-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="7efd8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7efd8-110">EXAMPLES</span></span>

### <span data-ttu-id="7efd8-111">Örnek 1: geçerli depolama hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="7efd8-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="7efd8-112">Bu komut belirtilen aboneliğin varsayılan depolama hesabını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7efd8-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="7efd8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7efd8-113">PARAMETERS</span></span>

### <span data-ttu-id="7efd8-114">-Context</span><span class="sxs-lookup"><span data-stu-id="7efd8-114">-Context</span></span>
<span data-ttu-id="7efd8-115">Geçerli depolama hesabı için bir **Azurestoragecontext** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7efd8-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="7efd8-116">Depolama bağlamı nesnesi edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7efd8-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UsingStorageContext
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7efd8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7efd8-117">-DefaultProfile</span></span>
<span data-ttu-id="7efd8-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7efd8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7efd8-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="7efd8-119">-Name</span></span>
<span data-ttu-id="7efd8-120">Bu cmdlet 'in değiştirdiği depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7efd8-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7efd8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7efd8-121">-ResourceGroupName</span></span>
<span data-ttu-id="7efd8-122">Değiştirilecek depolama hesabını içeren kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7efd8-122">Specifies the resource group that contains the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7efd8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7efd8-123">CommonParameters</span></span>
<span data-ttu-id="7efd8-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7efd8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7efd8-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7efd8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7efd8-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7efd8-126">INPUTS</span></span>

### <span data-ttu-id="7efd8-127">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="7efd8-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="7efd8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7efd8-128">System.String</span></span>

## <span data-ttu-id="7efd8-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7efd8-129">OUTPUTS</span></span>

### <span data-ttu-id="7efd8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7efd8-130">System.String</span></span>

## <span data-ttu-id="7efd8-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7efd8-131">NOTES</span></span>

## <span data-ttu-id="7efd8-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7efd8-132">RELATED LINKS</span></span>

[<span data-ttu-id="7efd8-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7efd8-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


