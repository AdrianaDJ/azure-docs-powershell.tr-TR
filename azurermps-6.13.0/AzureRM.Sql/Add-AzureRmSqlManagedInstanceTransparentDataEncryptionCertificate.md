---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: 9fe8e36a752b4643ba44a59e8c44954bf25284c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762578"
---
# <span data-ttu-id="0ef77-101">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="0ef77-101">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="0ef77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ef77-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef77-103">Verilen yönetilen örnek için saydam veri şifreleme sertifikası ekler</span><span class="sxs-lookup"><span data-stu-id="0ef77-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ef77-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ef77-104">SYNTAX</span></span>

```
Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ef77-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ef77-105">DESCRIPTION</span></span>
<span data-ttu-id="0ef77-106">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate, verilen yönetilen örneğe saydam bir veri şifreleme sertifikası ekler</span><span class="sxs-lookup"><span data-stu-id="0ef77-106">The Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="0ef77-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ef77-107">EXAMPLES</span></span>

### <span data-ttu-id="0ef77-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0ef77-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="0ef77-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ef77-109">PARAMETERS</span></span>

### <span data-ttu-id="0ef77-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef77-110">-DefaultProfile</span></span>
<span data-ttu-id="0ef77-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0ef77-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ef77-112">-Managedınstancename</span><span class="sxs-lookup"><span data-stu-id="0ef77-112">-ManagedInstanceName</span></span>
<span data-ttu-id="0ef77-113">Yönetilen örnek adı</span><span class="sxs-lookup"><span data-stu-id="0ef77-113">The managed instance name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef77-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0ef77-114">-PassThru</span></span>
<span data-ttu-id="0ef77-115">Başarılı bir yürütmede, eklenen sertifika nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="0ef77-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="0ef77-116">-Parola</span><span class="sxs-lookup"><span data-stu-id="0ef77-116">-Password</span></span>
<span data-ttu-id="0ef77-117">Saydam veri şifreleme sertifikasının parolası</span><span class="sxs-lookup"><span data-stu-id="0ef77-117">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef77-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="0ef77-118">-PrivateBlob</span></span>
<span data-ttu-id="0ef77-119">Saydam veri şifreleme sertifikası için özel blob</span><span class="sxs-lookup"><span data-stu-id="0ef77-119">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef77-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ef77-120">-ResourceGroupName</span></span>
<span data-ttu-id="0ef77-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0ef77-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="0ef77-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="0ef77-122">-Confirm</span></span>
<span data-ttu-id="0ef77-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0ef77-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ef77-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ef77-124">-WhatIf</span></span>
<span data-ttu-id="0ef77-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ef77-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ef77-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0ef77-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ef77-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef77-127">CommonParameters</span></span>
<span data-ttu-id="0ef77-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ef77-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef77-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ef77-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef77-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ef77-130">INPUTS</span></span>

### <span data-ttu-id="0ef77-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0ef77-131">None</span></span>

## <span data-ttu-id="0ef77-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ef77-132">OUTPUTS</span></span>

### <span data-ttu-id="0ef77-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0ef77-133">System.Boolean</span></span>

## <span data-ttu-id="0ef77-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ef77-134">NOTES</span></span>

## <span data-ttu-id="0ef77-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ef77-135">RELATED LINKS</span></span>
