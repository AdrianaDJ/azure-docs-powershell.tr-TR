---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e26d8aa68fd7ffcbab45073b845352feae83aea5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266849"
---
# <span data-ttu-id="c1493-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c1493-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="c1493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1493-102">SYNOPSIS</span></span>
<span data-ttu-id="c1493-103">Verilen yönetilen örnek için saydam veri şifreleme sertifikası ekler</span><span class="sxs-lookup"><span data-stu-id="c1493-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="c1493-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1493-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1493-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1493-105">DESCRIPTION</span></span>
<span data-ttu-id="c1493-106">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate, verilen yönetilen örneğe saydam bir veri şifreleme sertifikası ekler</span><span class="sxs-lookup"><span data-stu-id="c1493-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="c1493-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1493-107">EXAMPLES</span></span>

### <span data-ttu-id="c1493-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c1493-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="c1493-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1493-109">PARAMETERS</span></span>

### <span data-ttu-id="c1493-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1493-110">-DefaultProfile</span></span>
<span data-ttu-id="c1493-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c1493-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1493-112">-Managedınstancename</span><span class="sxs-lookup"><span data-stu-id="c1493-112">-ManagedInstanceName</span></span>
<span data-ttu-id="c1493-113">Yönetilen örnek adı</span><span class="sxs-lookup"><span data-stu-id="c1493-113">The managed instance name</span></span>

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

### <span data-ttu-id="c1493-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c1493-114">-PassThru</span></span>
<span data-ttu-id="c1493-115">Başarılı bir yürütmede, eklenen sertifika nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="c1493-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="c1493-116">-Parola</span><span class="sxs-lookup"><span data-stu-id="c1493-116">-Password</span></span>
<span data-ttu-id="c1493-117">Saydam veri şifreleme sertifikasının parolası</span><span class="sxs-lookup"><span data-stu-id="c1493-117">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="c1493-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="c1493-118">-PrivateBlob</span></span>
<span data-ttu-id="c1493-119">Saydam veri şifreleme sertifikası için özel blob</span><span class="sxs-lookup"><span data-stu-id="c1493-119">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="c1493-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1493-120">-ResourceGroupName</span></span>
<span data-ttu-id="c1493-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c1493-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="c1493-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="c1493-122">-Confirm</span></span>
<span data-ttu-id="c1493-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c1493-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1493-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1493-124">-WhatIf</span></span>
<span data-ttu-id="c1493-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1493-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1493-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c1493-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1493-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1493-127">CommonParameters</span></span>
<span data-ttu-id="c1493-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1493-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1493-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c1493-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1493-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1493-130">INPUTS</span></span>

### <span data-ttu-id="c1493-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c1493-131">None</span></span>

## <span data-ttu-id="c1493-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1493-132">OUTPUTS</span></span>

### <span data-ttu-id="c1493-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1493-133">System.Boolean</span></span>

## <span data-ttu-id="c1493-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1493-134">NOTES</span></span>

## <span data-ttu-id="c1493-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1493-135">RELATED LINKS</span></span>
