---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273815"
---
# <span data-ttu-id="cbf59-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cbf59-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="cbf59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbf59-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf59-103">Azure depolama hesabı için erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="cbf59-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="cbf59-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cbf59-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbf59-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cbf59-105">DESCRIPTION</span></span>
<span data-ttu-id="cbf59-106">**Get-AzStorageAccountKey** cmdlet 'ı bir Azure depolama hesabının erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="cbf59-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="cbf59-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cbf59-107">EXAMPLES</span></span>

### <span data-ttu-id="cbf59-108">Örnek 1: depolama hesabının erişim anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="cbf59-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="cbf59-109">Bu komut belirtilen Azure depolama hesabı için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="cbf59-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="cbf59-110">Örnek 2: depolama hesabı için belirli bir erişim anahtarı alma</span><span class="sxs-lookup"><span data-stu-id="cbf59-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="cbf59-111">Örnek 3: depolama hesabının erişim tuşlarını listeler, Kerberos anahtarlarını içerir (Active Directory etkinleştirilmişse)</span><span class="sxs-lookup"><span data-stu-id="cbf59-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="cbf59-112">Bu komut belirtilen Azure depolama hesabı için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="cbf59-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="cbf59-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cbf59-113">PARAMETERS</span></span>

### <span data-ttu-id="cbf59-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf59-114">-DefaultProfile</span></span>
<span data-ttu-id="cbf59-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cbf59-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbf59-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="cbf59-116">-ListKerbKey</span></span>
<span data-ttu-id="cbf59-117">Belirtilen depolama hesabı için (Active Directory etkinleştirilmişse) Kerberos anahtarlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="cbf59-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="cbf59-118">Kerberos anahtarı, Azure dosyaları kimliği tabanlı kimlik doğrulaması için Azure Active Directory etki alanı hizmeti (Azure AD DS) veya Active Directory etki alanı hizmeti (AD DS) ile depolama hesabı başına oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="cbf59-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="cbf59-119">Depolama hesabını temsil eden etki alanı hizmetine kaydedilen kimliğin parolası olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cbf59-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="cbf59-120">Kerberos anahtarı, depolama hesabında tüm denetim veya veri düzlemi okuma veya yazma işlemlerini gerçekleştirme izni sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="cbf59-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

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

### <span data-ttu-id="cbf59-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="cbf59-121">-Name</span></span>
<span data-ttu-id="cbf59-122">Bu cmdlet 'in anahtarları aldığı depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cbf59-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf59-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbf59-123">-ResourceGroupName</span></span>
<span data-ttu-id="cbf59-124">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cbf59-124">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf59-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf59-125">CommonParameters</span></span>
<span data-ttu-id="cbf59-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cbf59-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf59-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbf59-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf59-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cbf59-128">INPUTS</span></span>

### <span data-ttu-id="cbf59-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cbf59-129">System.String</span></span>

## <span data-ttu-id="cbf59-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cbf59-130">OUTPUTS</span></span>

### <span data-ttu-id="cbf59-131">Microsoft. Azure. Management. Storage. model. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cbf59-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="cbf59-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cbf59-132">NOTES</span></span>

## <span data-ttu-id="cbf59-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cbf59-133">RELATED LINKS</span></span>

[<span data-ttu-id="cbf59-134">Yeni-Azstoragekey</span><span class="sxs-lookup"><span data-stu-id="cbf59-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


