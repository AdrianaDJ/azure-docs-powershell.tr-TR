---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
ms.openlocfilehash: 73680e82a9d898075e905d88bcc8602609a5612d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762673"
---
# <span data-ttu-id="6f5e6-101">Set-AzureRmCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f5e6-101">Set-AzureRmCurrentStorageAccount</span></span>

## <span data-ttu-id="6f5e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f5e6-102">SYNOPSIS</span></span>
<span data-ttu-id="6f5e6-103">Belirtilen aboneliğin geçerli depolama hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-103">Modifies the current Storage account of the specified subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f5e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f5e6-104">SYNTAX</span></span>

### <span data-ttu-id="6f5e6-105">UsingResourceGroupAndNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6f5e6-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzureRmCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f5e6-106">Storagecontext 'i</span><span class="sxs-lookup"><span data-stu-id="6f5e6-106">UsingStorageContext</span></span>
```
Set-AzureRmCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f5e6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f5e6-107">DESCRIPTION</span></span>
<span data-ttu-id="6f5e6-108">**Set-AzureRmCurrentStorageAccount** cmdlet 'ı, Azure PowerShell 'de belirtilen Azure aboneliğinin geçerli Azure Depolama hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-108">The **Set-AzureRmCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="6f5e6-109">Depolama hesabı adı belirtmeden depolama alanına eriştiğinizde geçerli depolama hesabı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-109">The current storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="6f5e6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f5e6-110">EXAMPLES</span></span>

### <span data-ttu-id="6f5e6-111">Örnek 1: geçerli depolama hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6f5e6-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzureRmCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="6f5e6-112">Bu komut belirtilen aboneliğin varsayılan depolama hesabını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-112">This command sets the default storage account for the specified subscription.</span></span>

## <span data-ttu-id="6f5e6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f5e6-113">PARAMETERS</span></span>

### <span data-ttu-id="6f5e6-114">-Context</span><span class="sxs-lookup"><span data-stu-id="6f5e6-114">-Context</span></span>
<span data-ttu-id="6f5e6-115">Geçerli depolama hesabı için bir **Azurestoragecontext** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="6f5e6-116">Depolama bağlamı nesnesi edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-116">To obtain a storage context object, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6f5e6-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="6f5e6-117">-Name</span></span>
<span data-ttu-id="6f5e6-118">Bu cmdlet 'in değiştirdiği depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-118">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6f5e6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f5e6-119">-ResourceGroupName</span></span>
<span data-ttu-id="6f5e6-120">Değiştirilecek depolama hesabını içeren kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-120">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="6f5e6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f5e6-121">-DefaultProfile</span></span>
<span data-ttu-id="6f5e6-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f5e6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f5e6-123">CommonParameters</span></span>
<span data-ttu-id="6f5e6-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f5e6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f5e6-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f5e6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f5e6-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f5e6-126">INPUTS</span></span>

## <span data-ttu-id="6f5e6-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f5e6-127">OUTPUTS</span></span>

## <span data-ttu-id="6f5e6-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f5e6-128">NOTES</span></span>

## <span data-ttu-id="6f5e6-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f5e6-129">RELATED LINKS</span></span>

[<span data-ttu-id="6f5e6-130">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f5e6-130">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


