---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ca7f0f87ebcbad3d613939f2e73a743763b134c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280226"
---
# <span data-ttu-id="083e6-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="083e6-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="083e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="083e6-102">SYNOPSIS</span></span>
<span data-ttu-id="083e6-103">Anahtar Kasası için sertifika bildirimleri için kaydedilmiş kişileri alır.</span><span class="sxs-lookup"><span data-stu-id="083e6-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="083e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="083e6-104">SYNTAX</span></span>

### <span data-ttu-id="083e6-105">VaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="083e6-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="083e6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="083e6-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="083e6-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="083e6-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="083e6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="083e6-108">DESCRIPTION</span></span>
<span data-ttu-id="083e6-109">**Get-Azanahtarvaultcertificatecontact** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir Anahtar Kasası için sertifika bildirimleri için kaydedilmiş kişileri alır.</span><span class="sxs-lookup"><span data-stu-id="083e6-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="083e6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="083e6-110">EXAMPLES</span></span>

### <span data-ttu-id="083e6-111">Örnek 1: tüm sertifika kişilerini alma</span><span class="sxs-lookup"><span data-stu-id="083e6-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="083e6-112">Bu komut contoso tuş Kasası 'ndaki sertifika nesneleri için tüm kişileri alır ve $Contacts değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="083e6-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="083e6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="083e6-113">PARAMETERS</span></span>

### <span data-ttu-id="083e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="083e6-114">-DefaultProfile</span></span>
<span data-ttu-id="083e6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="083e6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="083e6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="083e6-116">-InputObject</span></span>
<span data-ttu-id="083e6-117">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="083e6-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="083e6-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="083e6-118">-ResourceId</span></span>
<span data-ttu-id="083e6-119">Tuş Kasası kimliği.</span><span class="sxs-lookup"><span data-stu-id="083e6-119">KeyVault Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083e6-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="083e6-120">-VaultName</span></span>
<span data-ttu-id="083e6-121">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="083e6-121">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083e6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083e6-122">CommonParameters</span></span>
<span data-ttu-id="083e6-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="083e6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083e6-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="083e6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083e6-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="083e6-125">INPUTS</span></span>

### <span data-ttu-id="083e6-126">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="083e6-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="083e6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="083e6-127">System.String</span></span>

## <span data-ttu-id="083e6-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="083e6-128">OUTPUTS</span></span>

### <span data-ttu-id="083e6-129">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="083e6-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="083e6-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="083e6-130">NOTES</span></span>

## <span data-ttu-id="083e6-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="083e6-131">RELATED LINKS</span></span>

[<span data-ttu-id="083e6-132">Add-Azanahtarvaultcertificatecontact</span><span class="sxs-lookup"><span data-stu-id="083e6-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="083e6-133">Remove-Azanahtarvaultcertificatecontact</span><span class="sxs-lookup"><span data-stu-id="083e6-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

