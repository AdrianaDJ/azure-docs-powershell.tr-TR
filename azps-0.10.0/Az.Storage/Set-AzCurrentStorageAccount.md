---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: 87a24efbd5fca423d700ab01dd78765fd6d595bc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936172"
---
# <span data-ttu-id="aa2e7-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa2e7-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="aa2e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="aa2e7-103">Belirtilen aboneliğin geçerli depolama hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="aa2e7-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="aa2e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa2e7-104">SYNTAX</span></span>

### <span data-ttu-id="aa2e7-105">UsingResourceGroupAndNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aa2e7-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa2e7-106">Storagecontext 'i</span><span class="sxs-lookup"><span data-stu-id="aa2e7-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa2e7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa2e7-107">DESCRIPTION</span></span>
<span data-ttu-id="aa2e7-108">**Set-AzCurrentStorageAccount** cmdlet 'ı, Azure PowerShell 'de belirtilen Azure aboneliğinin geçerli Azure Depolama hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="aa2e7-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="aa2e7-109">Depolama hesabı adı belirtmeden depolama alanına eriştiğinizde geçerli depolama hesabı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="aa2e7-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="aa2e7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa2e7-110">EXAMPLES</span></span>

### <span data-ttu-id="aa2e7-111">Örnek 1: geçerli depolama hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="aa2e7-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="aa2e7-112">Bu komut belirtilen aboneliğin varsayılan depolama hesabını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="aa2e7-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="aa2e7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa2e7-113">PARAMETERS</span></span>

### <span data-ttu-id="aa2e7-114">-Context</span><span class="sxs-lookup"><span data-stu-id="aa2e7-114">-Context</span></span>
<span data-ttu-id="aa2e7-115">Geçerli depolama hesabı için bir **Azurestoragecontext** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa2e7-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="aa2e7-116">Depolama bağlamı nesnesi edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="aa2e7-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="aa2e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa2e7-117">-DefaultProfile</span></span>
<span data-ttu-id="aa2e7-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aa2e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2e7-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="aa2e7-119">-Name</span></span>
<span data-ttu-id="aa2e7-120">Bu cmdlet 'in değiştirdiği depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa2e7-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="aa2e7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa2e7-121">-ResourceGroupName</span></span>
<span data-ttu-id="aa2e7-122">Değiştirilecek depolama hesabını içeren kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa2e7-122">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="aa2e7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa2e7-123">CommonParameters</span></span>
<span data-ttu-id="aa2e7-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa2e7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa2e7-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa2e7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa2e7-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa2e7-126">INPUTS</span></span>

### <span data-ttu-id="aa2e7-127">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="aa2e7-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="aa2e7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="aa2e7-128">System.String</span></span>

## <span data-ttu-id="aa2e7-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa2e7-129">OUTPUTS</span></span>

### <span data-ttu-id="aa2e7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="aa2e7-130">System.String</span></span>

## <span data-ttu-id="aa2e7-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa2e7-131">NOTES</span></span>

## <span data-ttu-id="aa2e7-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa2e7-132">RELATED LINKS</span></span>

[<span data-ttu-id="aa2e7-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa2e7-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)

